# Mimo Code VS Code 插件

[English](README.md)

将 [Mimo Code](https://mimo.xiaomi.com/zh/mimocode/start) 无缝集成到 VS Code 开发工作流中。

## 前置要求

本插件需要在系统中安装 [Mimo Code CLI](https://mimo.xiaomi.com/zh/mimocode/start)。

## 安装方式

1. 打开 VS Code
2. 打开命令面板（`Cmd+Shift+P` / `Ctrl+Shift+P`）
3. 输入 **"Extensions: Install from VSIX..."**
4. 选择 `mimo-code-plugin-1.0.0.vsix` 文件

## 功能特性

- **快速启动**：使用 `Cmd+Shift+1`（Mac）/ `Ctrl+Shift+1`（Windows/Linux）在分屏终端中打开 Mimo Code，若已打开则自动聚焦。
- **新建会话**：使用 `Cmd+Shift+Esc`（Mac）/ `Ctrl+Shift+Esc`（Windows/Linux）启动新的终端会话。也可点击编辑器标题栏的 Mimo Code 按钮。
- **上下文感知**：自动将当前选中的代码或文件传递给 Mimo Code。
- **文件引用快捷键**：使用 `Cmd+Shift+2`（Mac）/ `Ctrl+Shift+2`（Windows/Linux）插入文件引用（如 `@src/file.ts#L10-20`）。

## 命令列表

| 命令 | 说明 | 快捷键 |
|------|------|--------|
| Open mimo code | 打开或聚焦已有终端 | `Cmd+Shift+1` / `Ctrl+Shift+1` |
| Open mimo code in new tab | 始终打开新终端 | `Cmd+Shift+Esc` / `Ctrl+Shift+Esc` |
| Add Filepath to Terminal | 在光标处插入文件引用 | `Cmd+Shift+2` / `Ctrl+Shift+2` |

## 问题反馈

如遇到问题或有改进建议，请在 https://github.com/wuyujiesong/mimo-code-plugin/issues 提交 issue。

## 开发指南

1. 用 VS Code 打开项目目录
2. 运行 `npm install` 安装依赖
3. 按 `F5` 启动插件调试窗口

### 修改代码

调试期间 `tsc` 和 `esbuild` 的文件监听会自动运行，代码修改后在后台重新构建。

查看修改效果：

1. 在调试窗口中打开命令面板（`Cmd+Shift+P` / `Ctrl+Shift+P`）
2. 运行 **Developer: Reload Window**

## 许可证

MIT
