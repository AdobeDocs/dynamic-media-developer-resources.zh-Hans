---
description: “ 2016年秋季版Adobe Scene7的最新发行说明，是Adobe Marketing Cloud中Adobe Experience Manager解决方案的一部分。”
solution: Experience Manager
title: Scene7 2016年秋季版本
feature: Dynamic Media Classic
role: Developer,Business Practitioner
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 0%

---

# Scene7 2016年秋季版本{#scene-fall-release}

Adobe Scene7 2016年秋季版本部分的最新发行说明，内容涉及Adobe Marketing Cloud中的Adobe Experience Manager解决方案。

## Scene7 2016年秋季版本 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Marketing Cloud]中[!DNL Adobe Experience Manager]解决方案的[!DNL Adobe Scene7] Fall 2016版本部分的最新发行说明。

* [常规](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [场景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [查看器（图像提供5.5.3）](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [查看器（图像提供5.5.2）](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [查看器（图像提供5.5.1）](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5查看器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2和图像渲染6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 常规 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很兴奋地宣布推出HTTP/2内容交付功能，这将带来性能提升的总体优势。

请参阅[HTTP2内容交付常见问题解答](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic)。

## Scene7发布系统 {#section-24487cb493444d808fb7193f0a00cdd4}

有关完整文档，请参阅[https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**新增功能、增强功能和错误修复**

* 从[!DNL Adobe Scene7 Publishing System]用户界面中删除了视频剪辑功能。
* 在必要和可能的情况下，为所有Scene7 Servlet添加了身份验证。
* 修复了与垃圾桶中的列表视图有关的错误。
* 出于安全考虑，已从用户管理中删除了&#x200B;**创建Dynamic Media Classic(Scene7)管理员**&#x200B;用户功能。
* FTP WebAdmin现在支持OKTA身份验证。
* 删除了为新Media Portal用户创建的默认密码功能。
* 错误修复，涉及在添加新用户时生成的临时密码。 密码不符合必要的密码要求。
* 解决了WebAdmin根磁盘已满的问题。
* 错误修复，涉及禁用用户，使其不会立即反映在用户界面中。
* 错误修复，涉及删除某个用户，但该用户稍后不允许您重新创建该用户。
* 修复了以下错误：向新Scene7用户发送的欢迎电子邮件，这些用户未包含用于控制某些设置的身份验证。
* 修复了以下错误：如果任何文件夹的名称中包含特殊字符，则无法检索FTP文件夹列表。
* 为Scene7环境配置OKTA服务提供程序。
* 添加了对查看器分析的Marketing Cloud组织ID的支持。
* 已实施Scene7 SAML使用者。

## 查看器（图像提供5.5.3） {#section-1d59bcd5825d487b80b59a6d1a08ed30}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**图像提供5.5.3的错误修复**

* 与RequireJS和DOJO库的兼容性。

   在查看器部署期间进行整合的SDK JS缓存。

## 查看器（图像提供5.5.2） {#section-9932c988cfee45749594af481dfc6476}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**图像提供5.5.2的错误修复**

* 在Windows 7的Internet Explorer 11中播放视频失败。
* `initialframe` 未影响HTML5 eCatalog移动设备上的纵向模式。

## 查看器（图像提供5.5.1） {#section-833ab92c91c941d2bfdc27f233f582ad}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**Image Serving 5.5.1的新增功能、增强功能和错误修复**

* 具有搜索功能的HTML5 eCatalog查看器。
* 添加了HLS流视频播放作为大多数桌面系统的默认视频交付方法。 基于Flash的HDS视频流仍可用作替代播放选项。
* 添加了对运行Chrome浏览器且具有鼠标和触摸输入的设备的支持。
* 向Analytics集成添加了Marketing Cloud组织ID支持。
* 将AppMeasurement JavaScript库更新到版本1.6.1。
* 在eCatalog查看器中增加了对从右到左方向的支持。
* 修复了`tip=0,-1,0`导致范围外错误的问题。

**兼容性说明**

* Blackberry

   * 与旧版AVS集不兼容。 客户端可能需要重新上传AVS集以允许播放。

* 常规

   * 当用户放大到页面时，浏览器端缩放可能会导致用户界面和图像变得模糊。 UI格式设置可能也会因缩放而显示不正确。 这将全屏显示。
   * 由于移动设备存在大小限制，混合媒体查看器使用幻灯片手势来交换嵌入图像集中的帧，而不是点按嵌入的色板组件。 该组件作为可视指示器存在。
   * 在Internet Explorer浏览器和某些触控设备中，全屏模式不占用整个设备屏幕。 而是将应用程序的大小调整为浏览器窗口的大小。
   * “关闭”按钮在iOS 8.0和8.1中不起作用，但在iOS 8.2中不再出现

* 银河二世

   * 缩放和eCatalog HTML5查看器出现内存泄漏。 在框架中重复导航可能会导致浏览器崩溃。
   * 双击查看器可能会导致整个页面缩放，而不是只显示启用了浏览器端缩放的查看器。

* 银河S4

   * 在纵向模式下，设备被检测为平板电脑，并在浏览器设置中选中全屏。

* Galaxy Nexus

   * 双击查看器可能会导致整个页面缩放，而不是只显示启用了浏览器端缩放的查看器。

* Galaxy Nexus 10和Galaxy平板电脑

   * 目录显示了具有纵向和横向方向的页面跨页不正确。

* HTC移动设备

   * 我们的发现显示，无法禁用本机捏合缩放是HTC UI包装器(HTC Sense)的“功能”。 当对查看器使用“捏合缩放”手势时，这可能会导致整个页面缩放。 建议改用双击。
   * 如果图像映射较小且很接近，则图像映射图标可能会重叠。

* HTML5视频

   * Internet Explorer 9:自定义海报图像不显示。
   * `IntialBitRate` 仅软件HLS和FlashHDS播放支持修饰符。当播放使用本机播放器时，该函数不起作用。
   * 目前不支持OGG和WebM渐进式播放。
   * 浏览器缩放可能会导致视频播放器以不正确的大小显示（包括Windows OS控制面板显示设置）
   * 在Safari上使用HLS流播放的视频搜寻可能不一致。

* Internet Explorer

   * 目前不支持Quirks模式。
   * 当前不支持兼容模式。
   * 当前不支持移动设备上的Internet Explorer。

* iOS

   * 大型eCatalog可能导致iPad 2上的浏览器崩溃。
   * 查看器会将iPhone 6+手机检测为平板电脑。

* Safari

   * Safari 6.1或更高版本：Internet插件设置可能会阻止Flash视频播放。
   * 在Safari上使用HLS流播放的视频“搜寻”可能不一致。
   * 无法在使用HLS流的Safari 6上查找视频的结尾。

**已知问题和限制**

* 从`iscommands`开始的图像服务修饰符不会按设计添加到`req=set`请求中。 仅影响图像显示的修饰符可以正常工作。 影响大小的修改量必须用于复杂资产。 例如，

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] 关闭鼠标后，FlyoutIE9有时会停留在屏幕上。
* 浏览器缩放会导致调整大小错误。
* iPad 2:大型eCatalog资产会在iOS上导致Safari崩溃。
* 所有查看器

   * 不支持水印、模糊处理和锁定。
   * 不支持图像预设。
   * 目前不支持使用`display:none` CSS或通过从父节点动态分离查看器来在DOM中添加或删除查看器。

* HTML5所有查看器

   * 在表格中嵌入查看器可能会导致在非本机全屏模式下查看器的大小或位置不正确。 建议改用DIV。
   * 代码中具有显式实例名称的参数要求URL中的实例名称并被覆盖（例如，`zoomView.iconfeffect=0`）。
   * 当前不支持图像提供命令裁剪。
   * 仅当查看器在子窗口中打开时，“关闭”按钮才可工作。
   * `iscommands`修饰符不支持影响图像大小的图像服务修饰符。

* HTML5 eCatalog

   * 导航到其他HTML页面并返回时，查看器有时会重置回第一页。
   * 旋转iOS设备后，页面布局有时显示不正确。 放大页面可更正布局。
   * 内部仅链接到多页面跨页中最左侧的页面。 在纵向模式下影响移动设备。
   * InitalFrame仅链接到多页跨页中最左侧的页面。 在纵向模式下影响移动设备。
   * 由于浏览器限制，打印功能在IE9中不可用。

* HTML5混合媒体

   * 当前不支持音轨播放。

* HTML5 Social

   * 要在传出电子邮件中正确呈现缩略图，`serverurl`修饰符必须具有绝对URL。

* HTML5视频

   * 海报图像可能会遇到“最大大小”错误。 公司可能需要提高图像服务发布的限制设置。
   * 如果托管HTML页面的是从外部服务器(而不是Scene7服务器)提供，则视频字幕需要公司规则集。 请联系Adobe支持以获取帮助。
   * 由于缓冲，Analytics跟踪可能会报告不正确的播放百分比
   * 在iPad或Android设备上，可能会显示黑帧而不是海报图像。
   * 在iPad或Android设备上加载查看器期间，黑帧可能会在屏幕上闪烁。
   * 当在iPad设备上将背景设置为白色/透明时，VideoPlayer组件的侧面会显示黑色边框。
   * 在使用iOS 7的iPad上，视频的最后一帧可能会失真。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式下，在视频搜寻期间，可能会偶尔发生宏阻塞。
      * 首次访客时，海报图像可能无法在Microsoft Edge浏览器中显示。
      * 当使用渐进式播放时，在Internet Explorer 9中加载视频后，海报图像可能会隐藏。

## Scene7 HTML5查看器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

用户指南位于客户端安装的AdobeHTML5查看器SDK文件夹中。 组件API文档可在客户端安装的文档子文件夹中找到。

**3.0.2的错误修复**

* VideoPlayer — 在Windows 7的Internet Explorer 11中播放视频失败
* TableOfContents - `initialframe`不影响HTML5 eCatalog查看器在移动设备上的纵向模式。

**3.0.1的新增功能、增强功能和错误修复**

* 常规

   * 添加了HLS流视频播放作为大多数桌面系统的默认视频交付方法。 基于Flash的HDS视频流仍可用作替代播放选项。
   * 添加了SearchManager、SearchPanel、SearchEffect和SearchButton组件，以支持eCatalog查看器中的新搜索功能。
   * 添加了对在Chrome浏览器上同时运行鼠标和触摸输入的设备的支持。
   * 重构了Android版本检测以支持将来版本的操作系统
   * 在特定于eCatalog的SDK组件中添加对从右到左方向的支持。

* 控制栏

   * 为ControlBar内容添加了可选滚动功能，以防内容不适合可用宽度。

* FlyoutzoomView

   * 修复了`tip=0,-1,0`导致范围外错误的情况。

**兼容性说明**

* Android 4.x

   * 要禁用默认设置，需要为组件添加以下CSS规则时，应以蓝色突出显示：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * 当在AVS集中更改比特率流时，视频播放可能停止。

* 铬黄

   * 由于Chrome的内部缓存，任何强制组件重建的API调用都可能会被忽略。

* 银河二世

   * 查看器有时无法加载到全屏。
   * 此时，Pageview在设备上出现内存泄漏问题。
   * 当浏览器端缩放处于活动状态时，双击手势会缩放查看器和页面。

* Galaxy Nexus

   * 某些视图组件上显示的工件。
   * 当浏览器端缩放处于活动状态时，双击手势会缩放查看器和页面。

* iPad 3

   * iPad 3的本机分辨率为2048x1536。 如果公司的IS发布、图像大小限制设置为低于此值，则这可能会导致显示问题。

* iPhone4

   * 在滚动页面后，图标效果重播图标被替换为播放图标。

* Internet Explorer

   * 在IE 10及更早的全屏模式下，不会占用整个屏幕，而是只会将应用程序的大小调整为浏览器窗口的大小。
   * 不支持Quirks呈现模式。
   * 当前不支持移动设备上的Internet Explorer。
   * 如果异步包含，则加载Util.js可能会失败。
   * IconEffect图标会阻止SpinView和ZoomView组件上的点击事件。

* 本机设备视频播放器

   * 当使用VideoPlayer调用设备的本机播放器时，不支持在VideoPlayer上分层UI组件。
   * 在Safari 6中，本机模式下的视频播放不一致。
   * 在滚动页面后，本机播放将重播图标替换为播放图标。

* 触控设备

   * 全屏模式不占用整个设备屏幕，而是只将应用程序的大小调整为浏览器窗口的大小。
   * 自定义游标在触屏设备上不起作用。
   * 目前不支持在触控设备上缩放页面。 嵌入HTML5查看器需要具有相应设置的视区元标记。

* Xoom

   * 当浏览器端缩放处于活动状态时，双击手势会缩放查看器和页面。

**已知问题和限制**

* 所有组件

   * 在版本2.7.2及更早版本中，使用`insertBefore()` API将一些组件添加到DOM中。 因此，无论何时创建组件实例相对于其他组件，这些组件都会置于堆叠顺序的底部。 在2.8.1版本中，所有组件现在都使用`appendChild()` API，这意味着组件堆叠顺序与实例创建顺序匹配。

   * 不支持使用`iscommand`修饰符设置图像Alpha通道格式。 请改用组件`FMT`参数。
   * 当前不支持CSS转换属性。

* 触控设备

   * 触控设备上的捏合手势不会生成缩放事件

* 容器

   * 不支持容器上的边框、内边距和边距。 Adobe建议向父DIV添加样式元素。
   * 需要显式设置容器大小，否则组件的大小可能会正确。

* 打印组件

   * 由于浏览器限制，在Internet Explorer 9中，打印组件可能无法正确缩放纸张上的内容。

* IconEffect组件

   * 如果`autohide`处于禁用状态（设置为`0`），则IconEffect会在Internet Explorer上生成脚本错误。

* ImageMapEffect组件

   * 在视图组件上平移图像时，会延迟使用重新定位图标。

* MediaSet组件

   * 内联资产请求与URL上的编码相同。

* NavigationView组件

   * 当前组件不支持调整大小。

* PageScrubber组件

   * 在iPhone 5中，当PageScrubber气泡设置为文本时，当按钮沿轨道滑动时，会显示伪影。 在样式中使用`-webkit-background-clip: content;`可解决此问题。

* SpinView组件

   * 在图像旋转时，在轻扫手势并旋转设备后，SpinView有时会出现冻结状态。

* 色板组件

   * 选择越界色板时，会显示2个高亮显示。
   * 使用`selectSwatch()`方法自动滚动时无法正常工作。

* VideoPlayer

   * 如果将搜寻设置为100%，而回退设置为自动，则不会更新视频帧。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式下，在视频搜寻期间，可能会偶尔出现宏阻塞。
   * 首次访客时，海报图像可能无法在Microsoft Edge浏览器中显示。
   * 当使用渐进式播放时，在Internet Explorer 9中加载视频后，海报图像可能会隐藏。

## Dynamic Media图像提供6.3.2和图像呈现6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC实用程序 — 不再支持`downsample2x2`标记。 此标记质量较差，IPS不再使用2x2下采样器。
* CORS标头 — 当前，为`/is/content/`请求配置了CORS标头。
