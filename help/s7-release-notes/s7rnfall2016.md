---
description: Adobe Scene72016年秋季版本的最新发行说明是Adobe Marketing CloudAdobe Experience Manager解决方案的一部分。
solution: Experience Manager
title: Scene72016年秋发布
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '2231'
ht-degree: 0%

---


# Scene72016年秋发布{#scene-fall-release}

Adobe Scene72016年秋季版本的最新发行说明是Adobe Marketing CloudAdobe Experience Manager解决方案的一部分。

## Scene72016年秋发布{#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Marketing Cloud]中[!DNL Adobe Experience Manager]解决方案的[!DNL Adobe Scene7] 2016年秋季版本部分的最新发行说明。

* [常规](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [场景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [查看器（图像服务5.5.3）](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [查看器（图像服务5.5.2）](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [查看器（图像服务5.5.1）](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5查看器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media经典图像服务6.3.2和图像渲染6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 常规 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe兴奋地宣布推出HTTP/2投放的内容，同时提高性能的整体优势。

请参阅[HTTP2投放内容常见问题解答](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic)。

## Scene7出版系统{#section-24487cb493444d808fb7193f0a00cdd4}

有关完整文档，请参阅[https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**新增功能、增强和错误修复**

* 从[!DNL Adobe Scene7 Publishing System]用户界面删除了视频剪辑功能。
* 在必要和可能的情况下，为所有Scene7Servlet添加身份验证。
* 涉及垃圾桶中列表视图的错误修复。
* 出于安全考虑，已从用户管理中删除了&#x200B;**创建Dynamic Media经典(Scene7)管理员**&#x200B;用户功能。
* FTP WebAdmin现在支持OKTA身份验证。
* 删除了为新Media Portal用户创建的默认密码的功能。
* 错误修复，涉及添加新用户时生成的临时密码。 密码不符合必要的密码要求。
* 解决了WebAdmin根磁盘已满的问题。
* 涉及禁用用户的错误修复不会立即反映在用户界面中。
* 涉及删除用户的错误修复，该用户不允许您稍后重新创建用户。
* 错误修复，涉及发送给未包含身份验证的新Scene7用户的欢迎电子邮件以控制某些设置。
* 错误修复：如果文件夹名称中有特殊字符，则无法检索FTP文件夹列表。
* 为Scene7服务提供商配置OKTA环境。
* 增加了对查看器分析Marketing Cloud组织ID的支持。
* 实施了Scene7SAML消费者。

## 查看器（图像服务5.5.3）{#section-1d59bcd5825d487b80b59a6d1a08ed30}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**图像服务5.5.3的错误修复**

* 与RequireJS和DOJO库的兼容性。

   在查看器部署期间整合的SDK JS缓存。

## 查看器（图像服务5.5.2）{#section-9932c988cfee45749594af481dfc6476}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**图像服务5.5.2的错误修复**

* 在Windows 7上的Internet Explorer 11中播放视频失败。
* `initialframe` 未影响HTML5 eCatalog的移动设备上的纵向模式。

## 查看器（图像服务5.5.1）{#section-833ab92c91c941d2bfdc27f233f582ad}

有关完整文档，请参阅[查看器参考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**Image Serving 5.5.1的新增功能、增强和错误修复**

* 具有搜索功能的HTML5 eCatalog查看器。
* 添加了HLS流视频播放作为大多数桌面系统的默认视频投放方法。 基于Flash的HDS视频流仍可用作替代播放选项。
* 添加了对同时运行Chrome浏览器的鼠标和触摸输入设备的支持。
* 为Analytics集成添加了Marketing Cloud组织ID支持。
* 将AppMeasurement JavaScript库更新至版本1.6.1。
* 在eCatalog查看器中增加了对从右到左方向的支持。
* 修复了`tip=0,-1,0`导致超出范围错误的问题。

**兼容性说明**

* Blackberry

   * 与旧AVS集不兼容。 客户端可能需要重新上传AVS集才能进行播放。

* 常规

   * 当用户放大到页面时，浏览器侧缩放可能会导致UI和图像变得模糊。 根据缩放情况，UI格式可能显示不正确。 这将转换为全屏。
   * 由于移动设备的大小限制，混合媒体查看器使用幻灯片手势来交换嵌入图像集中的帧，而不是点击嵌入的色板组件。 该组件作为可视指示器存在。
   * 在Internet Explorer浏览器和某些触控设备中，全屏模式不占用整个设备屏幕。 而是根据浏览器窗口的大小调整应用程序大小。
   * “关闭”按钮不能用于iOS 8.0和8.1，但不再出现在iOS 8.2中

* Galaxy SII

   * 缩放和电子目录HTML5查看器出现内存泄漏。 在框架中重复导航可能导致浏览器崩溃。
   * 多次点击查看器可能会导致整个页面缩放，而不是只有启用了浏览器侧缩放的查看器。

* Galaxy S4

   * 在纵向模式下检测到设备为平板电脑，并在浏览器设置中选中“全屏”。

* Galaxy Nexus

   * 多次点击查看器可能会导致整个页面缩放，而不是只有启用了浏览器侧缩放的查看器。

* Galaxy Nexus 10和Galaxy Tablet

   * 电子目录显示带有纵向和横向的不正确页面跨页。

* HTC移动设备

   * 我们的发现显示，无法禁用本机手指开合缩放是HTC UI(HTC Sense)包装器的“功能”。 这可能导致在查看器上使用“手指开合缩放”手势时整个页面缩放。 建议改用多次点击。
   * 如果图像映射很小并且很接近，则图像映射图标可能会重叠。

* HTML5视频

   * Internet Explorer 9:自定义海报图像不显示。
   * `IntialBitRate` 只有软件HLS和FlashHDS回放才支持修改程序。当播放使用本机播放器时，它不工作。
   * 目前不支持OGG和WebM渐进式播放。
   * 浏览器缩放可能导致视频播放器以不正确的大小显示（包括Windows OS控制面板显示设置）
   * 在Safari上使用HLS流进行视频搜索可能不一致。

* Internet Explorer

   * 此时不支持Quirks模式。
   * 目前不支持兼容性模式。
   * 目前不支持移动设备上的Internet Explorer。

* iOS

   * 较大的eCatalog可能导致iPad 2上的浏览器崩溃。
   * 查看器会将iPhone 6+手机检测为平板电脑。

* Safari

   * Safari 6.1或更高版本：Internet插件设置可能会阻止Flash视频回放。
   * 在Safari上使用HLS流的视频“搜索”可能不一致。
   * 无法在使用HLS流的Safari 6上寻找视频结束。

**已知问题和限制**

* `iscommands`中的图像服务修饰符不会按设计添加到`req=set`请求中。 仅影响图像显示的修饰符可以正常工作。 影响大小的修改量必须用于复杂资产。 例如，

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [关] 闭鼠标后，FlyoutIE9有时仍保留在屏幕上。
* 浏览器缩放会导致错误的大小调整。
* iPad 2:大型eCatalog资源将使iOS上的Safari崩溃。
* 所有查看器

   * 不支持水印、模糊处理和锁定。
   * 不支持图像预设。
   * 目前不支持使用`display:none` CSS或通过从父节点动态分离来在DOM中添加或删除查看器。

* HTML5所有查看器

   * 将查看器嵌入表中可能会导致查看器在非本机全屏模式下的大小调整或位置不正确。 建议改用DIV。
   * 代码中具有显式实例名称的参数要求URL中的实例名称也被覆盖（例如，`zoomView.iconfeffect=0`）。
   * 此时不支持图像服务命令裁剪。
   * 仅当查看器在子窗口中打开时，“关闭”按钮才起作用。
   * `iscommands`修饰符不支持影响图像大小的图像服务修饰符。

* HTML5电子目录

   * 导航到其他HTML页面并返回时，查看器偶尔会重置回第一页。
   * 旋转iOS设备后，页面布局偶尔会显示不正确。 放大页面可校正布局。
   * 内部链接仅指向多页跨页中最左侧的页面。 以纵向模式影响移动设备。
   * InitalFrame仅链接到多页跨页中最左侧的页面。 以纵向模式影响移动设备。
   * 由于浏览器的限制，打印功能在IE9中不可用。

* HTML5混合媒体

   * 当前不支持音轨播放。

* HTML5 Social

   * 要在传出电子邮件中正确呈现缩略图，`serverurl`修饰符必须具有绝对URL。

* HTML5视频

   * 海报图像可能遇到“最大大小”错误。 公司可能需要增加图像服务发布的限制设置。
   * 如果从外部服务器(而非Scene7服务器)提供托管HTML页面的视频字幕，则视频字幕需要公司规则集。 联系Adobe支持寻求帮助。
   * 由于缓冲，分析跟踪可能报告播放百分比不正确
   * 黑框（而非海报图像）可能显示在iPad或Android设备上。
   * 在iPad或Android设备上加载查看器时，黑框可能在屏幕上闪烁。
   * 当背景在iPad设备上设置为白色／透明时，VideoPlayer组件一侧显示黑色边框。
   * 在使用iOS 7的iPad上，视频的最后一帧可能会失真。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式中进行视频搜索时，可能会偶尔发生宏阻止。
      * 海报图像在Microsoft Edge浏览器中可能首次不显示访客。
      * 在Internet Explorer 9中加载视频后，当使用渐进式回放时，海报图像可能会隐藏。

## Scene7HTML5查看器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

《用户指南》位于客户端安装的AdobeHTML5查看器SDK文件夹中。 组件API文档位于客户端安装的docs子文件夹中。

**3.0.2的错误修复**

* VideoPlayer —— 在Windows 7上的Internet Explorer 11中播放视频失败
* TableOfContents - `initialframe`不影响HTML5 eCatalog查看器的移动设备上的纵向模式。

**3.0.1的新增功能、增强和错误修复**

* 常规

   * 添加了HLS流视频播放作为大多数桌面系统的默认视频投放方法。 基于Flash的HDS视频流仍可用作替代播放选项。
   * 添加了SearchManager、SearchPanel、SearchEffect和SearchButton组件以支持电子目录查看器中的新搜索功能。
   * 增加了对在Chrome浏览器上同时运行鼠标和触摸输入的设备的支持。
   * 重构了Android版本检测以支持未来版本的操作系统
   * 在电子目录特定的SDK组件中添加对从右到左方向的支持。

* ControlBar

   * 为ControlBar内容添加了可选滚动，以防其不适合可用宽度。

* 浮动缩放视图

   * 修复了`tip=0,-1,0`导致超出范围错误的情况。

**兼容性说明**

* Android 4.x

   * 要禁用默认值，需要为组件添加以下CSS规则：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * 当在AVS集中更改比特率流时，视频播放可以停止。

* 铬黄

   * 由于Chrome的内部缓存，强制进行组件重建的任何API调用都可能被忽略。

* Galaxy SII

   * 查看器有时无法加载到全屏。
   * 此时，Pageview在设备上发生内存泄漏。
   * 多次点按手势可在浏览器端缩放处于活动状态时缩放查看器和页面。

* Galaxy Nexus

   * 某些视图组件上显示的伪像。
   * 多次点按手势可在浏览器端缩放处于活动状态时缩放查看器和页面。

* iPad 3

   * iPad 3的本机分辨率为2048x1536。 如果公司的IS发布（图像大小限制设置为低于此限制），则这可能会导致显示问题。

* iPhone4

   * 在滚动页面后，图标效果重播图标替换为播放图标。

* Internet Explorer

   * 在IE 10及更早的全屏模式中，它不占用整个屏幕，而只是将应用程序调整为浏览器窗口的大小。
   * 不支持Quirks渲染模式。
   * 目前不支持移动设备上的Internet Explorer。
   * 如果异步包含，Util.js可能无法加载。
   * 图标效果图标块单击SpinView和ZoomView组件上的事件。

* 本机设备视频播放器

   * 当VideoPlayer用于调用设备的本机播放器时，不支持在VideoPlayer上分层UI组件。
   * 在Safari 6上，以本机模式播放视频的操作不一致。
   * 滚动页面后，本机播放将重放图标替换为播放图标。

* 触控设备

   * 全屏模式不占用整个设备屏幕，而是只将应用程序大小调整为浏览器窗口的大小。
   * 自定义光标在触控设备上不工作。
   * 目前不支持在触控设备上缩放页面。 嵌入HTML5查看器需要具有相应设置的viewport meta标记。

* Xoom

   * 多次点按手势可在浏览器端缩放处于活动状态时缩放查看器和页面。

**已知问题和限制**

* 所有组件

   * 在版本2.7.2及更早版本中，使用`insertBefore()` API将一些组件添加到DOM。 因此，无论何时创建组件实例相对于其他组件，这些组件都会将自己置于堆叠顺序的底部。 在2.8.1版本中，所有组件现在都在使用`appendChild()` API，这意味着组件堆叠顺序将与实例创建顺序匹配。

   * 不支持使用`iscommand`修饰符设置图像alpha渠道格式。 请改用组件`FMT`参数。
   * 目前不支持CSS转换属性。

* 触控设备

   * 触控设备上的手指开合手势不会生成缩放事件

* 容器

   * 不支持容器上的边框、边距和边距。 Adobe建议向父DIV添加样式元素。
   * 需要显式设置容器大小，否则可以正确调整组件大小。

* 打印组件

   * 由于浏览器的限制，在Internet Explorer 9中，打印组件可能无法在纸张上正确缩放内容。

* IconEffect组件

   * 如果`autohide`被禁用（设置为`0`）,IconEffect会在Internet Explorer上生成脚本错误。

* ImageMapEffect组件

   * 在视图组件上平移图像时，重新定位图标会延迟。

* 媒体集组件

   * 内联资产请求与URL上的编码相同。

* NavigationView组件

   * 当前组件不支持调整大小。

* PageScrubber组件

   * 在iPhone 5上，当PageScrubber气泡设置为文本时，它在按轨道滑动按钮时显示伪影。 在样式中使用`-webkit-background-clip: content;`可解决该问题。

* 旋转视图组件

   * 在图像旋转时，在轻扫手势和旋转设备后，SpinView有时会冻结。

* 色板组件

   * 选择越界色板时，将显示2个高亮。
   * 使用`selectSwatch()`方法的自动滚动工作不正确。

* VideoPlayer

   * 如果搜索设置为100%且回退设置为自动，则视频帧不会更新。
   * 在Chrome、Firefox和Internet Explorer浏览器的HLS流模式中进行视频搜索时，可能会偶尔出现宏阻止。
   * 海报图像在Microsoft Edge浏览器中可能首次不显示访客。
   * 在Internet Explorer 9中加载视频后，当使用渐进式回放时，海报图像可能会隐藏。

## Dynamic Media图像服务6.3.2和图像渲染6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* 不再支持IC实用程序- `downsample2x2`标志。 此标志是质量较差的2x2下采样器，IPS不再使用它。
* CORS头——当前，为`/is/content/`请求配置了CORS头。

