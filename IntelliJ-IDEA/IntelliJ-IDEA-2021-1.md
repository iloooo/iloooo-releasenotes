
# IntelliJ IDEA 2021.1 正式发布！快来看看又有哪些神仙功能加入

https://mp.weixin.qq.com/s/ffGaBvdiOd54olSeMdOT6g

**「IntelliJ IDEA 2021.1 EAP」**版本已经发布了很久，就在今天，终于等到正式版的发布。这个大版本最大的更新内容，就是支持WSL 2和JAVA 16了。而且除了支持WSL 2，也支持其他形式的“ssh 远程运行”，就像clion那样；让你的java程序开发在本地，而运行在远程。

赶紧来看看，2021年这个大版本有哪些更新内容吧！

## WSL 2的支持

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/019deb0fad644052880a7b0618504f4b~tplv-k3u1fbpfcp-zoom-1.image)

**「都说Windows 是Linux最好的发行版，可是你的IDE不支持WSL运行那又有何用呢？」**

现在IDEA 终于支持了WSL 2，让我们可以再Windows 上开发，而运行在 WSL 2环境下，像JDK、构建环境（maven/gradle）都可以是WSL 2系统中的，实在太爽了。以后就可以完全用WSL 2来进行开发了，日常Windows，所有开发环境全部wsl，而且文件系统也是打通的，完全没理由拒绝！

详细的Windows 10 安装WSL 2的教程，可以参见微软的官方文档，跟着文档一步步来就可以了，非常简单。

文档链接：

https://docs.microsoft.com/en-us/windows/wsl/install-win10

## 运行目标

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/260a696680834aaabab391ad79360756~tplv-k3u1fbpfcp-zoom-1.image)

运行目标，这个功能太香了。我们的程序不光可以运行在本地，在WSL 2，在远程SSH主机，还可以再Docker中，一键运行在Docker。

而且Docker 对WSL 2的支持也非常好，我们还可以运行在WSL 2中的Docker，同时用Windows 中的Docker管理工具，真香！

## 内置的HTML预览器

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a67b0fc08f634744af6f585de88a7e45~tplv-k3u1fbpfcp-zoom-1.image)

在HTML文件中，只需要点击右上角的IDEA图标，就可以使用内置预览器去预览网页了，而且实时刷新，再也不用打开浏览器预览。

## 搜索范围的增强

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/706b2ce56c734af88faf198480cf58b6~tplv-k3u1fbpfcp-zoom-1.image)



以后我们在搜索时，还可以添加外部的依赖到作用域中，完成更全面的搜索。设置入口在`Preferences/Settings | Appearance & Behavior | Scopes`

## Windows 版本的任务栏增强

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ffbb4184cc554c508843af34aaf0f730~tplv-k3u1fbpfcp-zoom-1.image)



在任务栏中，对IDEA右键会出现最近的项目

## 增强的Pull Request支持

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8b8238b578b645b085eefedf653d94eb~tplv-k3u1fbpfcp-zoom-1.image)



你的提交PR操作，以后只需要在Pull Request面板中进行了，再也不用命令和网页

## 支持 Git 提交模板

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8b8238b578b645b085eefedf653d94eb~tplv-k3u1fbpfcp-zoom-1.image)



## 和其他分支对比文件

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/cfc8f774e7b241d9af0b3c0741630daa~tplv-k3u1fbpfcp-zoom-1.image)



现在可以再\_Compare with branch\_弹框中，与其他分支对比文件了

## 拆分窗口优化

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/19d3961532b34848956ae6ab5cb5e804~tplv-k3u1fbpfcp-zoom-1.image)

垂直分割编辑器窗口后，双击Tab就可以将当前窗口最大化，再次双击会还原

## JSON Path的支持

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/18bb51506cd7484a8931d69ddc00149e~tplv-k3u1fbpfcp-zoom-1.image)

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/db7fa145eec941ee9e9b0ce7ecbd210d~tplv-k3u1fbpfcp-zoom-1.image)

以后打开`.json`文件时，就可以用JSON Path过滤/转换/输出了

## JAVA 16的支持

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/8cbd1cc2c8f340eb954ee9cbaf65a4c7~tplv-k3u1fbpfcp-zoom-1.image)

IDEA 2021.1 版本已经支持了JAVA 16

## 更智能的数据检查

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0de1815a1d1e44c4a426634acba42c99~tplv-k3u1fbpfcp-zoom-1.image)

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/cbf27ddda4f5493ba123af86f597fe5f~tplv-k3u1fbpfcp-zoom-1.image)

IDEA 现在会提示你一些基本的错误，比如数据长度为负数，提示你拆箱装箱等。

## 浅色UML背景的支持

![图1片](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/427527c9581d45409691a39357edda5c~tplv-k3u1fbpfcp-zoom-1.image)

对于一些喜欢用浅色主题的同学来说，以后看UML图再也不用深色了

好了，IDEA 2021.1 版本的主要新特性就这些，还有一些Docker/JavaScript/K8s的特性，

大家有兴趣可以浏览官方说明：https://www.jetbrains.com/idea/whatsnew/

