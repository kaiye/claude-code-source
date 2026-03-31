# 2026-03-31 Request Minimization And Routing

## 请求主链路
- [`src/query.ts`](../recovered/claude-code-original/src/query.ts) -> `deps.callModel`
- [`src/query/deps.ts`](../recovered/claude-code-original/src/query/deps.ts) -> `queryModelWithStreaming`
- [`src/services/api/claude.ts`](../recovered/claude-code-original/src/services/api/claude.ts) 组装请求体并调用 `anthropic.beta.messages.create(..., stream: true)`

核心结论：
- 请求体大小主要由 `system + messages + tools + thinking` 决定。
- 请求次数主要由 agent loop、tool loop、compact/retry/fallback 等路径决定。

## 纯配置降请求方案
建议默认组合：
- `--bare` 或 `CLAUDE_CODE_SIMPLE=1`
- `CLAUDE_CODE_ENABLE_PROMPT_SUGGESTION=0`
- `CLAUDE_CODE_DISABLE_AUTO_MEMORY=1`
- `DISABLE_AUTO_COMPACT=1`
- `--thinking disabled` 或 `CLAUDE_CODE_DISABLE_THINKING=1`

可选瘦身：
- `CLAUDE_CODE_DISABLE_CLAUDE_MDS=1`
- `CLAUDE_CODE_DISABLE_GIT_INSTRUCTIONS=1`
- `--system-prompt "<短提示词>"`
- `--tools ""`（会明显影响能力）

## zsh 覆盖函数
```zsh
claude(){ CLAUDE_CODE_SIMPLE=1 CLAUDE_CODE_ENABLE_PROMPT_SUGGESTION=0 CLAUDE_CODE_DISABLE_AUTO_MEMORY=1 DISABLE_AUTO_COMPACT=1 CLAUDE_CODE_DISABLE_CLAUDE_MDS=1 CLAUDE_CODE_DISABLE_GIT_INSTRUCTIONS=1 CLAUDE_CODE_DISABLE_THINKING=1 command claude --bare --thinking disabled --system-prompt 'You are a concise coding assistant. Keep context and output minimal.' "$@"; }
```

## 关于 `opusplan` 与 `/btw`
- `opusplan` 不是复杂度路由，只是 plan 模式倾向 Opus，其他模式走 Sonnet。
- `/btw` 本身是 forked LLM 请求，不适合做“零成本旁路分类”。

### 参考源码
- [`src/utils/model/model.ts`](../recovered/claude-code-original/src/utils/model/model.ts)
- [`src/utils/model/modelOptions.ts`](../recovered/claude-code-original/src/utils/model/modelOptions.ts)
- [`src/commands/btw/btw.tsx`](../recovered/claude-code-original/src/commands/btw/btw.tsx)
- [`src/utils/sideQuestion.ts`](../recovered/claude-code-original/src/utils/sideQuestion.ts)

## 推荐端云协同路由
1. 先用本地/自定义模型做复杂度评分。
2. 低复杂度走自定义模型。
3. 高复杂度走 `claude`（并叠加最小化参数）。

伪代码：
```bash
score = classifier(prompt)
if score >= THRESHOLD:
  run claude (minimized config)
else:
  run custom-model
```
