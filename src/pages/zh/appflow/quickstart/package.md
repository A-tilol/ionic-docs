---
title: '构建一个本地二进制文件'
previousText: '部署实时更新'
previousUrl: '/docs/appflow/quickstart/deploy'
nextText: '创建自动化'
nextUrl: '/docs/appflow/quickstart/automation'
---


接下来，我们将使用 [Ionic 软件包](/docs/appflow/package/intro) 服务构建一个 Android `调试` 二进制文件。

<blockquote>
  
<b>Note:</b> If you'd like to build an Android <b>Release</b> binary or <b>any</b> iOS binary, you'll need to
<a href="/docs/appflow/package/credentials">generate signing certificates</a>
and <a href="/docs/appflow/package/adding-credentials">upload them to the Appflow dashboard.</a>
</blockquote>

## 开始构建软件包

为了部署实时更新，您将首先需要创建 [部署版本](/docs/appflow/package/builds)。

这样做有两种方法：

* 点击 `开始从 <code>提交` 选项卡生成</code> 图标 ![从提交开始编译](/docs/assets/img/appflow/ss-start-package-build-commits.png)
* 点击右上角的 `新版本` 按钮 `构建 > 版本` 标签页 ![新建版本](/docs/assets/img/appflow/ss-new-package-build.png)

为您的构建选择正确的提交。 您可以指定以下几个必填字段和 个可选字段：

* **Target Platform** - The platform for your build (iOS or Android for a package build)
* [Build Stack](/docs/appflow/build-stacks) - The build stack where the job will run.
* [构建类型](/docs/appflow/package/build-types) - 给定平台的构建类型(见 [iOS 构建类型](/docs/appflow/package/build-types#ios-build-types) 或 [Android 构建类型](/docs/appflow/package/build-types#android-build-types))
* [Signing Certificate](/docs/appflow/package/credentials) - The signing certificate for the for the build (if required)
* [环境](/docs/appflow/automation/environments#custom-environments) - 用于自定义构建过程的环境
* [本机配置](/docs/appflow/package/native-configs) - 用来自定义您的应用程序配置

For the quickstart tutorial, select the `Android` platform, the `Latest` build stack and the `Debug` type build which requires no other configuration. 一旦构建开始，您可以在遇到错误时查看进度，查看 日志。

![正在运行 Web 版本](/docs/assets/img/appflow/gif-start-package-build.gif)

## 正在下载版本

<blockquote>
  
<b>注意：</b> 如果您在上一步中无法成功地完成构建。 您可以找到常见软件包构建错误的答案
<a href="https://ionic.zendesk.com/hc/en-us/categories/360000410494-Package" target="_blank">我们知识库的这一部分</a>。
</blockquote>

成功的软件包构建生成一个 iOS 二进制(`.ipa` 或 IPA) 或一个 Android 二进制(`.apk` 或 APK) 文件。 一旦你有一个成功的构建， 您可以下载它，以便您可以通过 点击构建页面右侧的 `伪影` 部分中的文件名来在设备上安装它，或者点击 `下载IPA/APK` 图标在 `Building > Builds` 选项卡。

![下载软件包版本](/docs/assets/img/appflow/ss-download-package-build.png)