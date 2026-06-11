# Mimo Code for VS Code

[中文说明](README.zh-CN.md)

A Visual Studio Code extension that integrates [Mimo Code](https://github.com/wuyujiesong/mimo-code) directly into your development workflow.

## Prerequisites

This extension requires the [Mimo Code CLI](https://github.com/wuyujiesong/mimo-code) to be installed on your system.

## Installation

1. Open VS Code
2. Open the Command Palette (`Cmd+Shift+P` / `Ctrl+Shift+P`)
3. Type **"Extensions: Install from VSIX..."**
4. Select the `mimo-code-plugin-1.0.0.vsix` file

## Features

- **Quick Launch**: Use `Cmd+Shift+1` (Mac) / `Ctrl+Shift+1` (Windows/Linux) to open Mimo Code in a split terminal, or focus an existing terminal if one is already running.
- **New Session**: Use `Cmd+Shift+Esc` (Mac) / `Ctrl+Shift+Esc` (Windows/Linux) to start a new terminal session. You can also click the Mimo Code button in the editor title bar.
- **Context Awareness**: Automatically share your current selection or tab with Mimo Code.
- **File Reference Shortcuts**: Use `Cmd+Shift+2` (Mac) / `Ctrl+Shift+2` (Windows/Linux) to insert file references (e.g. `@src/file.ts#L10-20`).

## Commands

| Command | Description | Shortcut |
|---------|-------------|----------|
| Open mimo code | Open or focus existing terminal | `Cmd+Shift+1` / `Ctrl+Shift+1` |
| Open mimo code in new tab | Always open a new terminal | `Cmd+Shift+Esc` / `Ctrl+Shift+Esc` |
| Add Filepath to Terminal | Insert file reference at cursor | `Cmd+Shift+2` / `Ctrl+Shift+2` |

## Support

If you encounter issues or have feedback, please create an issue at https://github.com/wuyujiesong/mimo-code-plugin/issues.

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
