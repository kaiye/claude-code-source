# Claude Code Feature Index

> 基于 `src/` 源文件整理，仅保留三列：feature、中文描述、源码链接。

| Feature | 中文描述 | 源码链接 |
|---|---|---|
| `KAIROS` | 持久助手 / 持续存在的助手能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/interactiveHelpers.tsx#L241> |
| `PROACTIVE` | 主动模式 / 后台沉睡代理能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/main.tsx#L2197> |
| `COORDINATOR_MODE` | 协调器模式 / 多 Agent 协作 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/coordinator/coordinatorMode.ts#L37> |
| `BRIDGE_MODE` | 桥接远控模式 / Remote Control | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/main.tsx#L2246> |
| `DAEMON` | 守护进程 / 会话监督能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L77> |
| `BG_SESSIONS` | 后台会话能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/main.tsx#L1116> |
| `ULTRAPLAN` | 超级规划模式 / 长时规划 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L104> |
| `BUDDY` | AI 伙伴 / 宠物伴侣模式 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L118> |
| `TORCH` | Torch 模式（具体用途仍偏黑盒） | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L107> |
| `WORKFLOW_SCRIPTS` | 工作流脚本 / 自动化流程能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/constants/tools.ts#L45> |
| `VOICE_MODE` | 语音模式 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L80> |
| `TEMPLATES` | 模板任务 / Job templates | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/query.ts#L69> |
| `CHICAGO_MCP` | 电脑控制 MCP / computer use 能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/main.tsx#L1477> |
| `UDS_INBOX` | Unix Socket 收件箱 / 本地 IPC 通信 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/main.tsx#L1910> |
| `REACTIVE_COMPACT` | 响应式压缩 / 实时 compact | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/query.ts#L15> |
| `CONTEXT_COLLAPSE` | 上下文折叠 / 智能收缩上下文 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/setup.ts#L295> |
| `HISTORY_SNIP` | 历史裁剪 / 对话片段压缩 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/tools.ts#L123> |
| `CACHED_MICROCOMPACT` | 缓存微压缩 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/constants/prompts.ts#L66> |
| `TOKEN_BUDGET` | Token 预算 / 每轮 token 配额 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/constants/prompts.ts#L538> |
| `EXTRACT_MEMORIES` | 记忆提取 / 后台抽取 memory | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/memdir/paths.ts#L65> |
| `OVERFLOW_TEST_TOOL` | 溢出测试工具 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/tools.ts#L107> |
| `TERMINAL_PANEL` | 终端面板 / 终端捕获能力 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/tools.ts#L113> |
| `WEB_BROWSER_TOOL` | Web 浏览器工具 / 浏览器自动化 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/tools.ts#L117> |
| `FORK_SUBAGENT` | 分叉子代理 / Agent Fork | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/commands.ts#L113> |
| `DUMP_SYSTEM_PROMPT` | 导出系统提示词 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/entrypoints/cli.tsx#L53> |
| `ABLATION_BASELINE` | 消融基线模式 / 研究基准模式 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/entrypoints/cli.tsx#L21> |
| `BYOC_ENVIRONMENT_RUNNER` | BYOC 环境运行器 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/entrypoints/cli.tsx#L226> |
| `SELF_HOSTED_RUNNER` | 自托管运行器 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/entrypoints/cli.tsx#L238> |
| `MONITOR_TOOL` | 监控工具 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/tools.ts#L39> |
| `CCR_AUTO_CONNECT` | CCR 自动连接 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/utils/config.ts#L39> |
| `MEMORY_SHAPE_TELEMETRY` | 记忆形态遥测 / memory 访问分析 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/memdir/findRelevantMemories.ts#L66> |
| `EXPERIMENTAL_SKILL_SEARCH` | 实验性技能搜索 | <https://github.com/kaiye/claude-code-source-learning/blob/main/recovered/claude-code-original/src/constants/prompts.ts#L95> |
