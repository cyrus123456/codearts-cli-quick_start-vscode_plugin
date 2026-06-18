# codearts-cli-quick_start-vscode_plugin

[中文说明](README.zh-CN.md)

A Visual Studio Code extension that integrates [CodeArts](https://codearts.huaweicloud.com/download.html) directly into your development workflow. It adds a quick-launch CodeArts CLI button to the toolbar on the right side of the editor tabs.

![Button position](<images/按钮位置.png>)

## Prerequisites

This extension requires the [CodeArts CLI](https://codearts.huaweicloud.com/download.html) to be installed on your system.

![CodeArts CLI Download](<images/codearts CLI官网下载.png>)

### Login-Free CLI Startup

You can start the CodeArts CLI without logging in by configuring environment variables according to the [Huawei Cloud CodeArts CLI documentation](https://support.huaweicloud.com/usermanual-cli/codeartsagent_cli_0026.html#codeartsagent_cli_0026__section1797214121314).

## Installation

1. Open VS Code
2. Open the Command Palette (`Cmd+Shift+P` / `Ctrl+Shift+P`)
3. Type **"Extensions: Install from VSIX..."**
4. Select the `codearts-cli-quick-start-vscode-plugin-1.0.1.vsix` file

## Features

- **Quick Launch**: Use `Cmd+Shift+1` (Mac) / `Ctrl+Shift+1` (Windows/Linux) to open CodeArts in a split terminal, or focus an existing terminal if one is already running.
- **New Session**: Use `Cmd+Shift+Esc` (Mac) / `Ctrl+Shift+Esc` (Windows/Linux) to start a new terminal session. You can also click the CodeArts button in the editor title bar.
- **Context Awareness**: Automatically share your current selection or tab with CodeArts.
- **File Reference Shortcuts**: Use `Cmd+Shift+2` (Mac) / `Ctrl+Shift+2` (Windows/Linux) to insert file references (e.g. `@src/file.ts#L10-20`).

## Commands

| Command | Description | Shortcut |
|---------|-------------|----------|
| Open CodeArts | Open or focus existing terminal | `Cmd+Shift+1` / `Ctrl+Shift+1` |
| Open CodeArts in new tab | Always open a new terminal | `Cmd+Shift+Esc` / `Ctrl+Shift+Esc` |
| Add Filepath to Terminal | Insert file reference at cursor | `Cmd+Shift+2` / `Ctrl+Shift+2` |

## Support

If you encounter issues or have feedback, please create an issue at https://github.com/CyrusRune/codearts-cli-quick_start-vscode_plugin/issues.

## Development

1. Open the project directory in VS Code
2. Run `npm install` to install dependencies
3. Press `F5` to launch the Extension Development Host

### Making Changes

The `tsc` and `esbuild` watchers run automatically during debugging. Changes are rebuilt in the background.

To see your changes:

1. In the debug VS Code window, open the Command Palette (`Cmd+Shift+P` / `Ctrl+Shift+P`)
2. Run **Developer: Reload Window**

## License

MIT