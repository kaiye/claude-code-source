# 2026-03-31 Source Recovery

## 输入
- [`node_modules/@anthropic-ai/claude-code/cli.js`](../node_modules/@anthropic-ai/claude-code/cli.js)
- [`node_modules/@anthropic-ai/claude-code/cli.js.map`](../node_modules/@anthropic-ai/claude-code/cli.js.map)

## 恢复结果
恢复目录：[recovered/claude-code-original/](../recovered/claude-code-original/)

- sourcemap-backed 文件总数：`4756`
- `src/` 文件：`1902`
- `vendor/` 文件：`4`
- `node_modules/`（打包依赖源码）：`2850`

## 关键入口
- [`src/entrypoints/cli.tsx`](../recovered/claude-code-original/src/entrypoints/cli.tsx)
- [`src/main.tsx`](../recovered/claude-code-original/src/main.tsx)
- [`src/entrypoints/mcp.ts`](../recovered/claude-code-original/src/entrypoints/mcp.ts)
- [`src/entrypoints/init.ts`](../recovered/claude-code-original/src/entrypoints/init.ts)

## 限制
- 构建配置类文件（例如原始根 `package.json`、`tsconfig`、构建脚本）若未进入 sourcemap，无法 1:1 恢复。
- 恢复后的路径语义做了归一化，源码内容可信，工程元信息未必完整。

## 参考
- [`recovered/claude-code-original/RECOVERY_NOTES.md`](../recovered/claude-code-original/RECOVERY_NOTES.md)
- [`recovered/claude-code-original/MANIFEST.json`](../recovered/claude-code-original/MANIFEST.json)
- [`recovered/claude-code-original/MANIFEST.files.json`](../recovered/claude-code-original/MANIFEST.files.json)
