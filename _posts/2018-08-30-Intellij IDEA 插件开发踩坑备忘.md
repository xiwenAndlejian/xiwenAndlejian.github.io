---
layout: post
title:  '踩坑备忘'
tags:
  - IntelliJ IDEA
  - 插件
  - 踩坑
overlay: purple
published: true
---
记录关于 `IntelliJ IDEA` 插件开发中所遇到的坑
{: .lead}
<!–-break-–>

# IntelliJ IDEA 插件开发

相关文档：

* [官方文档](http://www.jetbrains.org/intellij/sdk/docs/basics.html)

## 导入已有插件项目时，无法识别

* 检查 `Project Settings` 中 `Project` 的 `SDK` 是否使用正确，正确的 `SDK` 应该是 `IntelliJ IDEA XXXX`
* 检查 `Project Settings` 中 `Modules` 的 `Sources`（源码路径）以及 `Resources`（资源路径）设置 是否正确

## 调试相关

### 如何 Run/Debug 插件

![step1](/assets/img/2018_08_30_1.png)

选择`Plugin`
![step2](/assets/img/2018_09_11_1.png)

如果出现如下图所示，查找不到可使用的模块
![error1](/assets/img/2018_09_11_2.png)

则是`IntelliJ IDEA`打开工程时，识别失败，把工程当做一般的`Java`项目来识别而导致的。

[stack overflow解决方案](https://stackoverflow.com/questions/18278440/how-to-import-and-run-existing-plugins-from-intellij-community-edition-repo)

找到项目的`.iml`文件，将其中的`JAVA_MODULE`修改为`PLUGIN_MODULE`即可。
