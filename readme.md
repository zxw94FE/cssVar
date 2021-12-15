### 安装

本Demo使用`bruce-cli`进行驱动，`bruce-cli`是一个React/Vue应用自动化构建脚手架，有兴趣的同学可移步到[bruce-cli使用文档](https://github.com/JowayYoung/bruce-cli)。

- 先全局安装`bruce-cli`：`npm i -g bruce-cli` (**需要Node 10.0.0+**)
- 再安装本Demo依赖：`npm install`

> 如果安装失败

- 将npm源镜像设置为淘宝镜像：`npm config set registry https://registry.npm.taobao.org`
- 将sass源镜像设置为淘宝镜像：`npm config set sass-binary-site https://npm.taobao.org/mirrors/node-sass`
- 重新执行命令安装：`npm i -g bruce-cli`、`npm install`

### 运行

- 启动开发环境：`bruce b`后选择`开发环境`，选择想要的选项即可(**演示Demo**)
- 打包测试环境：`bruce b`后选择`测试环境`，选择想要的选项即可
- 打包生产环境：`bruce b`后选择`生产环境`，选择想要的选项即可

> 如有疑问或交流分享，可添加笔者微信一起讨论