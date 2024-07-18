![logo](.github/logo.png)

为开发人员和IT从业者提供的实用工具。[点击查看！](https://it-tools.tech)

## 功能和路线图

请查看[问题列表](https://github.com/CorentinTh/it-tools/issues)以了解待实现的功能。

有工具的想法？提交一个[功能请求](https://github.com/CorentinTh/it-tools/issues/new/choose)吧！

## 自托管

为您的家庭实验室提供自托管解决方案

**从Docker Hub获取：**

```sh
docker run -d --name it-tools --restart unless-stopped -p 8080:80 corentinth/it-tools:latest
```

**从GitHub Packages获取：**

```sh
docker run -d --name it-tools --restart unless-stopped -p 8080:80 ghcr.io/corentinth/it-tools:latest
```

**其他解决方案：**

- [Cloudron](https://www.cloudron.io/store/tech.ittools.cloudron.html)
- [Tipi](https://www.runtipi.io/docs/apps-available)
- [Unraid](https://unraid.net/community/apps?q=it-tools)

## 贡献

### 推荐的IDE设置

使用以下扩展安装[VSCode](https://code.visualstudio.com/)：

- [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)（并禁用Vetur）
- [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [i18n Ally](https://marketplace.visualstudio.com/items?itemName=lokalise.i18n-ally)

推荐的设置：

```json
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "i18n-ally.localesPaths": ["locales", "src/tools/*/locales"],
  "i18n-ally.keystyle": "nested"
}
```

### `.vue`导入的类型支持

TypeScript默认无法处理`.vue`导入的类型信息，因此我们用`vue-tsc`替代`tsc` CLI进行类型检查。在编辑器中，我们需要[TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin)来使TypeScript语言服务识别`.vue`类型。

如果独立的TypeScript插件速度不够快，Volar还实现了一个更高效的[Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669)。您可以通过以下步骤启用它：

1. 禁用内置的TypeScript扩展
   1. 通过VSCode命令面板运行`Extensions: Show Built-in Extensions`
   2. 找到`TypeScript and JavaScript Language Features`，右键单击并选择`Disable (Workspace)`
2. 通过命令面板运行`Developer: Reload Window`重新加载VSCode窗口。

### 项目设置

```sh
pnpm install
```

### 编译并热重载开发环境

```sh
pnpm dev
```

### 类型检查、编译并为生产环境压缩

```sh
pnpm build
```

### 使用[Vitest](https://vitest.dev/)运行单元测试

```sh
pnpm test
```

### 使用[ESLint](https://eslint.org/)进行代码检查

```sh
pnpm lint
```

### 创建新工具

要创建新工具，有一个脚本可以生成新工具的模板，只需运行：

```sh
pnpm run script:create:tool my-tool-name
```

它会在`src/tools`目录下创建相应的文件，并在`src/tools/index.ts`中导入。您只需将导入的工具添加到适当的类别并开发工具即可。

## 贡献者

非常感谢所有已经贡献的人！

[![contributors](https://contrib.rocks/image?repo=corentinth/it-tools)](https://github.com/corentinth/it-tools/graphs/contributors)

## 鸣谢

由[Corentin Thomasset](//corentin-thomasset.fr)用❤️编码。

本项目通过[vercel.com](https://vercel.com)持续部署。

贡献者图表由[contrib.rocks](https://contrib.rocks/preview?repo=corentinth/it-tools)生成。

<a href="https://www.producthunt.com/posts/it-tools?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-it&#0045;tools" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=345793&theme=light" alt="IT&#0032;Tools - Collection&#0032;of&#0032;handy&#0032;online&#0032;tools&#0032;for&#0032;devs&#0044;&#0032;with&#0032;great&#0032;UX | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
<a href="https://www.producthunt.com/posts/it-tools?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-it&#0045;tools" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=345793&theme=light&period=daily" alt="IT&#0032;Tools - Collection&#0032;of&#0032;handy&#0032;online&#0032;tools&#0032;for&#0032;devs&#0044;&#0032;with&#0032;great&#0032;UX | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

## 许可证

本项目采用[GNU GPLv3](LICENSE)许可证。
