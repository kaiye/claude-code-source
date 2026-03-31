# 2026-03-31 System Prompt Analysis (CN)

## 主文件
- [`recovered/claude-code-original/src/constants/prompts.ts`](../recovered/claude-code-original/src/constants/prompts.ts)
- 入口函数：`getSystemPrompt()`

该提示词是“多 section 拼装”，不是单个静态字符串。

## 结构概览（默认非 bare）
1. Intro（身份、目标、网络安全边界）
2. System（工具权限、hook、system-reminder、注入防护）
3. Doing tasks（工程执行原则：先读再改、少过度设计、如实汇报）
4. Executing actions with care（高风险动作先确认）
5. Using your tools（专用工具优先、并行工具调用）
6. Tone and style（简洁、引用 `file_path:line`）
7. Output efficiency（信息密度与沟通效率）
8. Dynamic sections（session guidance、memory、env、mcp 指令等）

## 动态段重点
- `session_specific_guidance`
- `memory`
- `env_info_simple`
- `language`
- `output_style`
- `mcp_instructions`
- `scratchpad`
- `function result clearing`

这些段会按会话和运行时状态变化。

## bare 模式差异
当 `CLAUDE_CODE_SIMPLE=1`（`--bare`）时，系统提示词退化为极简版本（身份 + CWD + Date），大幅减少 token。

## 子代理提示词
默认子代理提示词常量：`DEFAULT_AGENT_PROMPT`（同文件）。

## 相关文件
- [`recovered/claude-code-original/src/constants/cyberRiskInstruction.ts`](../recovered/claude-code-original/src/constants/cyberRiskInstruction.ts)
- [`recovered/claude-code-original/src/utils/systemPrompt.ts`](../recovered/claude-code-original/src/utils/systemPrompt.ts)
- [`recovered/claude-code-original/src/query.ts`](../recovered/claude-code-original/src/query.ts)
