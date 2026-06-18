# mimo-code-plugin 打包流程

## 前置条件

- Node.js / Bun
- 已安装依赖：`bun install`

## 开发

### 编译（开发模式）

```bash
bun run compile
```

执行类型检查 → lint → esbuild 打包，输出到 `dist/extension.js`（带 sourcemap）。

### 热更新监听

```bash
bun run watch:esbuild   # 监听源码变化，自动重新打包
bun run watch:tsc       # 监听类型变化
```

## 打包发布

### 生产构建

```bash
bun run package
```

等价于：`tsc --noEmit` → `eslint src` → `node esbuild.js --production`

产物：`dist/extension.js`（minified，无 sourcemap）

### 生成 .vsix 安装包

```bash
npx @vscode/vsce package
```

或全局安装后：

```bash
npm install -g @vscode/vsce
vsce package
```

产物：`mimo-code-plugin-1.0.0.vsix`

### 发布到 VS Code Marketplace

```bash
vsce publish
```

需要先 `vsce create-publisher`（publisher: `CyrusRune`）并配置 PAT。

## 本地安装

```bash
code --install-extension mimo-code-plugin-1.0.0.vsix
```

## 项目结构

```
├── src/extension.ts       # 入口源码
├── dist/extension.js      # 打包产物
├── images/
│   ├── icon.png           # 插件图标（128x128+）
│   ├── button-dark.svg    # 深色主题按钮
│   └── button-light.svg   # 浅色主题按钮
├── esbuild.js             # 打包配置
├── tsconfig.json          # TypeScript 配置
├── .vscodeignore          # 打包时排除的文件
└── package.json           # 插件清单
```

## 打包排除项（.vscodeignore）

打包时自动排除：`node_modules/`、`src/`、`*.ts`、`*.map`、`esbuild.js`、测试文件等。最终 .vsix 只包含 `dist/`、`images/`、`package.json` 等必要文件。