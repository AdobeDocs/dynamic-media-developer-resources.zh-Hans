---
title: Scene7 2016年秋季版本
description: “Adobe Scene7 2016年秋季版本的最新发行说明是Adobe Experience Cloud中Adobe Experience Manager解决方案的一部分。”
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2236'
ht-degree: 0%

---

# Scene7 2016年秋季版本{#scene-fall-release}

Adobe Experience Cloud中Adobe Scene7 2016年秋季版本Adobe Experience Manager解决方案的最新发行说明。

## Scene7 2016年秋季版本 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Experience Cloud]中[!DNL Adobe Experience Manager]解决方案的[!DNL Adobe Scene7] 2016年秋季发行版的最新发行说明。

* [常规](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [场景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [查看器（图像服务5.5.3）](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [查看器（图像服务5.5.2）](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [查看器（图像服务5.5.1）](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5查看器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic图像服务6.3.2和图像渲染6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 常规 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很高兴地宣布推出HTTP/2内容交付功能，并全面提升性能。

请参阅[HTTP2内容交付常见问题解答](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html?lang=zh-Hans#dynamic)。

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

有关完整文档，请参阅[https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=zh-Hans](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=zh-Hans)

**新增功能、增强功能和错误修复**

* 已从[!DNL Adobe Scene7 Publishing System]用户界面中删除视频剪辑功能。
* 在必要和可能的情况下，向所有Scene7 Servlet添加了身份验证
* 修复了垃圾桶中列表视图的错误。
* 出于安全考虑，已从“用户管理”中删除&#x200B;**创建Dynamic Media Classic (Scene7)管理员**&#x200B;用户功能。
* FTP WebAdmin现在支持OKTA身份验证。
* 删除了为新Media Portal用户创建的默认密码的功能。
* 修复了在添加新用户时生成的临时密码的错误。 密码不符合必需的密码要求。
* 已解决WebAdmin根磁盘已满的问题。
* 涉及禁用用户的错误修复不会立即反映在用户界面中。
* 修复了涉及删除用户的错误，此错误稍后不允许您重新创建用户。
* 修复了以下错误：向新增Scene7用户发送欢迎电子邮件，但该电子邮件不包括用于控制某些设置的身份验证。
* 修复了以下错误：如果任何文件夹的名称中包含特殊字符，则无法检索FTP文件夹列表。
* 为Scene7环境配置OKTA服务提供程序。
* 为查看器Analytics添加了对Experience Cloud组织ID的支持。
* 实施了Scene7 SAML消费者。

## 查看器（图像服务5.5.3） {#section-1d59bcd5825d487b80b59a6d1a08ed30}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=zh-Hans)。

**针对图像服务5.5.3的错误修复**

* 与RequireJS和DOJO库兼容。

  在查看器部署期间合并SDK JS缓存。

## 查看器（图像服务5.5.2） {#section-9932c988cfee45749594af481dfc6476}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=zh-Hans)。

**针对图像服务5.5.2的错误修复**

* 在Windows 7上的Internet Explorer 11中播放视频失败。
* `initialframe`不会影响HTML5 eCatalog在移动设备上的纵向模式。

## 查看器（图像服务5.5.1） {#section-833ab92c91c941d2bfdc27f233f582ad}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=zh-Hans)。

**图像服务5.5.1的新增功能、增强功能和错误修复**

* HTML5具有搜索功能的eCatalog查看器。
* 添加了HLS流视频播放作为大多数桌面系统的默认视频交付方法。 基于Flash的HDS视频流仍可用作替代播放选项。
* 为运行Chrome浏览器的同时具有鼠标和触摸输入的设备添加了支持。
* 为Analytics集成添加了Experience Cloud组织ID支持。
* 将AppMeasurementJavaScript库更新至版本1.6.1。
* 在eCatalog查看器中增加了从右至左方向的支持。
* 修复了`tip=0,-1,0`导致超出范围错误的问题。

**兼容性说明**

* BlackBerry®

   * 与旧版AVS集不兼容。 客户端必须重新上传AVS集以允许播放。

* 常规

   * 浏览器端缩放可能会导致在用户放大到页面时，UI和图像变得模糊。 UI格式也可能因缩放而显示不正确。 这种效果会延续到全屏。
   * 由于移动设备上的大小限制，混合媒体查看器使用滑动手势来交换嵌入图像集中的帧，而不是点按嵌入的样本组件。 该组件以可视指示器的形式存在。
   * 在Internet Explorer浏览器和某些触控设备中，全屏模式不会占用整个设备屏幕。 相反，它根据浏览器窗口的大小来调整应用程序的大小。
   * “关闭”按钮在iOS 8.0和8.1中不起作用，但在iOS 8.2中不再出现

* Galaxy SIII

   * 使用Zoom和eCatalogHTML5查看器时，出现内存泄漏。 反复浏览各帧可能会导致浏览器崩溃。
   * 双击查看器可能会导致整个页面缩放，而不是仅在启用了浏览器端缩放的查看器中缩放。

* Galaxy S4

   * 在浏览器设置中全屏检查的情况下，设备在纵向模式下被检测为Tablet。

* Galaxy Nexus

   * 双击查看器可能会导致整个页面缩放，而不是仅在启用了浏览器端缩放的查看器中缩放。

* Galaxy Nexus 10和Galaxy平板电脑

   * eCatalog显示错误的页面跨页，具有纵向和横向方向。

* HTC移动设备

   * HTC移动设备Adobe的调查结果显示，无法禁用本机捏合缩放是HTC UI包装器(HTC Sense)的“功能”。 当在查看器上使用“捏合缩放”手势时，此问题可能会导致整个页面缩放。 建议改用双击方式。
   * 如果图像映射很小并且很接近，则图像映射图标可能会重叠。

* HTML5视频

   * Internet Explorer 9：不显示自定义海报图像。
   * 仅软件HLS和FlashHDS播放支持`IntialBitRate`修饰符。 使用本机播放器播放时，此选项不起作用。
   * 当前不支持OGG和WebM渐进式播放。
   * 浏览器缩放可能会导致视频播放器的显示大小不正确（包括Windows操作系统控制面板的“显示”设置）。
   * 在Safari上使用HLS流播放的视频搜寻可能不一致。

* Internet Explorer

   * 当前不支持Quirks模式。
   * 当前不支持兼容模式。
   * 当前不支持移动设备上的Internet Explorer。

* iOS

   * 大型eCatalog可能会导致iPad 2上的浏览器崩溃。
   * 查看者检测到iPhone 6+手机为平板电脑。

* Safari

   * Safari 6.1或更高版本： Internet插件设置可能会阻止Flash视频播放。
   * 在Safari上使用HLS流播放的视频“搜寻”可能不一致。
   * 无法使用HLS流在Safari 6上搜寻视频结尾。

**已知问题和限制**

* 来自`iscommands`的图像服务修饰符未按设计添加到`req=set`请求中。 仅影响图像显示的修饰符工作正常。 必须在复杂资源中使用影响大小的修饰符。 例如︰

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* 鼠标关闭后，[弹出] IE9有时仍保留在屏幕上。
* 浏览器缩放会导致调整大小错误。
* iPad 2：大型eCatalog资源在iOS上崩溃Safari。
* 所有查看器

   * 不支持水印、模糊处理和锁定。
   * 不支持图像预设。
   * 当前不支持使用`display:none` CSS从DOM添加或删除查看器，也不支持通过将其从父节点动态分离来添加或删除查看器。

* HTML5所有查看器

   * 将查看器嵌入表中可能会导致在非本机全屏模式下查看器大小或放置位置不正确。 建议改用DIV。
   * 代码中具有显式实例名称的参数要求URL中的实例名称也被覆盖（例如，`zoomView.iconfeffect=0`）。
   * 当前不支持图像服务命令裁切。
   * 仅当在子窗口中打开查看器时，“关闭”按钮才有效。
   * `iscommands`修饰符不支持影响图像大小的图像服务修饰符。

* HTML5 eCatalog

   * 导航到其他HTML页面并偶尔返回会导致查看器重置回第一页。
   * 旋转iOS设备后，页面布局偶尔会显示不正确。 放大页面可更正布局。
   * 多页跨页中最左侧页面的内部链接。 影响纵向模式的移动设备。
   * InitialFrame仅链接到多页跨页中最左侧的页面。 影响纵向模式的移动设备。
   * 由于浏览器限制，打印功能在IE9中不可用。

* HTML5 MixedMedia

   * 不支持音轨播放。

* HTML5社交

   * 要在传出电子邮件中正确呈现缩略图，`serverurl`修饰符必须具有绝对URL。

* HTML5视频

   * 海报图像可能遇到“最大大小”错误。 公司必须增加图像服务Publish的限制。
   * 如果从外部服务器(而不是Scene7服务器)提供托管HTML页面，则视频字幕需要公司规则集。 请联系Adobe支持部门以获取帮助。
   * Analytics跟踪可能会由于缓冲而报告不正确的播放百分比
   * iPad或Android™设备上可能会显示黑色帧而不是海报图像。
   * 在iPad或Android™设备上加载查看器时，屏幕上可能会闪烁“黑框”。
   * 当iPad设备上的背景设置为白色/透明时，VideoPlayer组件的一侧会显示黑色边框。
   * 在使用iOS 7的iPad上，视频的最后一帧可能会失真。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式下搜索视频时，可能会出现偶尔的宏阻止。
      * 首次来访的访客可能无法在Microsoft® Edge浏览器中显示海报图像。
      * 当使用渐进式播放时，在Internet Explorer 9中加载视频后，海报图像可能会隐藏。

## Scene7HTML5查看器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

该用户指南位于客户端安装的AdobeHTML5查看器SDK文件夹中。 组件API文档可在客户端安装的文档子文件夹中找到。

针对3.0.2 **的**&#x200B;错误修复

* VideoPlayer — 在Windows 7上的Internet Explorer 11中播放视频失败。
* 目录 — `initialframe`未影响HTML5 eCatalog查看器的移动设备上的纵向模式。

**3.0.1的新增功能、增强功能和错误修复**

* 常规

   * 添加了HLS流视频播放作为大多数桌面系统的默认视频交付方法。 基于Flash的HDS视频流仍可用作替代播放选项。
   * 添加了SearchManager、SearchPanel、SearchEffect和SearchButton组件，以支持eCatalog查看器中的新“搜索”功能。
   * 添加了对在Chrome浏览器上运行鼠标和触摸输入的设备的支持。
   * 重构了Android™版本检测，以支持操作系统的未来版本。
   * 在特定于eCatalog的SDK组件中添加对从右到左方向的支持。

* 控件栏

   * 为ControlBar内容添加了可选的滚动，以防它不符合可用宽度。

* FlyoutzoomView

   * 修复了`tip=0,-1,0`导致超出范围错误的情况。

**兼容性说明**

* Android™ 4.x

   * 要禁用默认值，必须为组件添加蓝色突出显示以下CSS规则：

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * 在更改AVS集中的比特率流时，视频播放可能会停止。

* Chrome

   * 由于Chrome的内部缓存，任何强制组件重建的API调用都可能被忽略。

* Galaxy SIII

   * 有时，查看器无法全屏加载。
   * Pageview当前遇到设备内存泄漏问题。
   * 当浏览器端缩放处于活动状态时，双击手势可缩放查看器和页面。

* Galaxy Nexus

   * 显示在某些视图组件上的工件。
   * 当浏览器端缩放处于活动状态时，双击手势可缩放查看器和页面。

* IPAD 3

   * iPad 3的原始分辨率为2048x1536。 如果公司的IS发布、图像大小限制设置得较低，此分辨率可能会导致显示问题。

* IPHONE4

   * 滚动页面后，Iconeffect重播图标已替换为播放图标。

* Internet Explorer

   * 在IE 10和更旧的全屏模式中，它不会占用整个屏幕，而只是根据浏览器窗口的大小调整应用程序的大小。
   * 不支持Quirks渲染模式。
   * 当前不支持移动设备上的Internet Explorer。
   * 如果异步包含Util.js，则可能无法加载。
   * IconEffect图标阻止在SpinView和ZoomView组件上单击事件。

* 本机设备视频播放器

   * 使用VideoPlayer调用设备的本机播放器时，不支持通过VideoPlayer来分层UI组件。
   * 在Safari 6上，本机模式下的视频播放不一致。
   * 滚动页面后，本机播放将重放图标替换为播放图标。

* 触控设备

   * 全屏模式不会占用整个设备屏幕，它只是根据浏览器窗口的大小调整应用程序的大小。
   * 自定义游标在触控设备上不起作用。
   * 当前不支持触控设备上的页面缩放。 嵌入HTML5查看器需要具有适当设置的视区meta标记。

* Xoom

   * 当浏览器端缩放处于活动状态时，双击手势可缩放查看器和页面。

**已知问题和限制**

* 所有组件

   * 在版本2.7.2及更早版本中，某些组件是使用`insertBefore()` API添加到DOM中的。 因此，无论组件实例是相对于其他组件创建的，此类组件都将处于栈叠顺序的底部。 在2.8.1版本中，所有组件现在都使用`appendChild()` API，这意味着组件栈叠顺序将与实例创建顺序匹配。

   * 不支持使用`iscommand`修饰符设置图像Alpha通道格式。 请改用组件`FMT`参数。
   * 当前不支持CSS转换属性。

* 触控设备

   * 触控设备上的夹捏手势不会生成缩放事件

* 容器

   * 不支持容器上的边框、边距和边距。 Adobe建议将样式元素添加到父DIV。
   * 必须明确设置容器大小，否则组件大小可能会不正确。

* 打印组件

   * 由于浏览器限制，在Internet Explorer 9中，打印组件可能无法正确缩放纸张上的内容。

* IconEffect组件

   * 如果`autohide`被禁用（设置为`0`），则IconEffect会在Internet Explorer上生成脚本错误。

* ImageMapEffect组件

   * 在视图组件上平移图像时，重新定位图标出现延迟。

* 媒体集组件

   * 内联资源请求的编码与URL上的相同。

* NavigationView组件

   * 当前组件不支持调整大小。

* PageScrubber组件

   * 在iPhone 5上，当PageScrubber气泡设置为文本时，它会在沿轨道滑动按钮时显示构件。 在样式中使用`-webkit-background-clip: content;`可以解决此问题。

* 旋转视图组件

   * 旋转图像时，在轻扫手势并旋转设备后，SpinView有时看起来会冻结。

* 样本组件

   * 选择越界样本时，将显示两个高亮显示。
   * 使用`selectSwatch()`方法的自动滚动工作不正确。

* videoplayer

   * 如果将搜寻设置为100%并将回退设置为auto，则视频帧不会更新。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式下搜索视频时，可能会偶尔出现宏阻塞。
   * 首次来访的访客可能无法在Microsoft® Edge浏览器中显示海报图像。
   * 当使用渐进式播放时，在Internet Explorer 9中加载视频后，海报图像可能会隐藏。

## Dynamic Media图像服务6.3.2和图像渲染6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* 不再支持IC实用程序 — `downsample2x2`标志。 此标记是一个质量较差的2x2降采样器，IPS不再使用它。
* CORS标头 — 当前，已为`/is/content/`请求配置CORS标头。
