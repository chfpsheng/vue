vue-cli 3 与 2 版本有很大区别
vue-cli 3 的 github 仓库由原有独立的 github 仓库迁移到了 vue 项目下
vue-cli 3 的项目架构完全抛弃了 vue-cli 2 的原有架构，3 的设计更加抽象和简洁（此处后续可以详细介绍）
vue-cli 3 是基于 webpack 4 打造，vue-cli 2 还是 webapck 3
vue-cli 3 的设计原则是“0配置”
vue-cli 3 提供了 vue ui 命令，提供了可视化配置，更加人性化
由于 vue-cli 3 也学习了 rollup 的零配置思路，所以项目初始化后，没有了以前熟悉的 build 目录，也就没有了 webpack.base.config.js、webpack.dev.config.js 、webpack.prod.config.js 等配置文件。
那么，我们该如何去配置自己的项目了？

其实这一切都是因为 vue-cli 3 的项目初始化，帮开发者已经解决了 80% ，甚至绝大部分情形下的 webpack 配置。

上述功能就是由 @vue/cli-service 依赖去处理，当你打开 node_modules 目录下 @vue 中的 cli-service 看一眼，是不是找到了熟悉的感觉？

