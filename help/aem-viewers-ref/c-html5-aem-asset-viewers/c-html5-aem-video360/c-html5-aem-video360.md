---
description: HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码、从Scene7 Publishing System或AEM Dynamic Media交付的渐进式360视频流。
seo-description: HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码、从Scene7 Publishing System或AEM Dynamic Media交付的渐进式360视频流。
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360{#video}

HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码、从Scene7 Publishing System或AEM Dynamic Media交付的渐进式360视频流。

360度视频（也称为沉浸式视频或球形视频）是视频录制，其中同时录制每个方向的视图，使用全向摄像机或一组摄像机拍摄。 同时支持单个视频集和自适应视频集。 此外，查看器还支持使用外部位置托管的渐进式视频和HLS流。

360视频的建议宽高比为2:1。 不支持空间音效。 该查看器仅用于360个视频；尝试播放非360视频会导致视频播放失真。

查看器设计为可在支持HTML5视频的桌面和移动Web浏览器上使用。 查看器支持可选的社交共享工具。

当基础系统支持HLS格式时，Video360查看器在其默认配置中使用HTML5流视频播放。 在不支持HTML5流的系统上，查看器返回到HTML5渐进式视频投放。

查看器类型为517。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅 [系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360查看器表示主JavaScript文件和一组帮助文件（单个JavaScript包含该查看器在运行时下载的特定查看器、资源、CSS所使用的所有HTML5查看器SDK组件）。

HTML5 Video360查看器既可在弹出模式下使用IS-Viewer附带的生产就绪型HTML页面，也可在嵌入式模式下使用，在该模式下，查看器使用文档化的API集成到目标网页中。

配置和外观设置与本指南中介绍的其他查看器的配置和外观设置类似。 所有外观设计都通过自定义(CSS)层叠样式表实现。

请参 [阅所有查看器通用的命令参考——所有查看器通用的配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令参考- URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360视频内容要求比标准非360视频更高的编码设置。 换句话说，360个内容的分辨率必须高于非360个视频，才能实现相同的可感知质量。 建议您为360视频考虑以下自适应视频预设设置：

* 720p,2500 kbps
* 1080p,5000 kbps
* 1440p,6600 kbps

但是，请注意，提供使用这种高质量设置编码的视频需要在最终用户的设备上实现高带宽连接。

## 与Video360查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360查看器为视频回放提供一组标准用户界面控件，如播放／暂停按钮、视频擦洗器视频时间泡泡、播放时间／总时间指示器、音量控制和全屏按钮。 所有这些控件都分组到查看器用户界面最底部的控件栏中。

请注意，在触控设备上，卷控件在用户界面中是隐藏的，因为只有使用设备的硬件按钮才能控制卷。

当查看器在弹出模式下运行时，用户界面中不提供全屏按钮。

查看器还支持各种社交媒体共享工具。 用户界面中的单个按钮可用，当用户单击或点按时，该按钮将展开到共享工具栏中。 共享工具栏包含支持的每种类型的共享渠道的图标，如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个模态对话框，其中包含相应的数据输入表单。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频回放会自动暂停。 由于Web浏览器的安全限制，共享工具在全屏模式下不可用。

该查看器支持在VR头盔（如Oculus Go和Oculus Rift）、VR HMD（头戴式显示屏）安装（如Google Cardboard）和非VR启用设备（如未连接到VR HMD安装的桌面浏览器、平板电脑和手机）上播放360个视频。

在VR头戴式耳机上视图360视频内容无需其他配置。 查看器会自动检测VR头戴式耳机是否存在，并在视频内容顶部显示“VR”按钮。 激活此“VR”按钮会将视频渲染切换到VR模式。 查看器仅在支持WebVR的浏览器中支持VR渲染。

要使用VR HMD安装，必须将修 `Video360Player.vrrender` 饰符设置为查看器 `1` 的配置，这会强制进行立体渲染。

在VR耳机和VR HMD上，视图点变化会响应于耳机移动而发生，而不是在VR模式中提供其他回放控制。

在未启用VR的设备上观看360个视频时，最终用户可以使用鼠标、触摸或键盘控制视频回放和视图点。

查看器支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入，但此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

查看器完全可通过键盘访问。 请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看器行为的需求不同。 有时网页会提供链接，单击该链接后，将在单独的浏览器窗口中打开查看器。 在其他情况下，必须将查看器直接嵌入到托管页面。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同的内容，或针对不同的浏览器窗口大小显示不同的内容。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 在大多数情况下，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，会自动暂停第一个视频。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回视频并继续播放。 此规则的唯一例外是Android 4.x设备上的Chrome浏览器，它可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式是移动设备上最常见的模式。 网页使用 `window.open()` JavaScript调用、正确配置的 `A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 它被调用， [!DNL Video360Viewer.html] 并且位于标准IS查看 [!DNL html5/] 器部署的子文件夹下：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以通过应用自定义CSS实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式中，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常只占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器的大小变化 `DIV`。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页调整其容器的方式而异 `DIV`。 如果网页仅设置容器的宽度，并且高度不受限制，则查看器会根据所使用的资产的长宽比自动选择其高度。 `DIV`此功能可确保资产完美适合视图，且两侧没有填充。 此用例是使用响应式Web设计布局框架（如Bootstrap、Foundation等）的网页中最常见的用例。

否则，如果网页同时设置查看器容器的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 `DIV`一个很好的示例是将查看器嵌入到模态叠加中，其中叠加根据Web浏览器窗口大小进行大小调整。

**固定大小嵌入**

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含该查看器 [!DNL Video360Viewer.js]。 该文 [!DNL Video360Viewer.js] 件位于标准IS查看 [!DNL html5/js/] 器部署的子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并且从同一域提供该查看器，则可以使用相对路径。 否则，您将指定一个安装了IS查看器的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查 `include` 看器JavaScript文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用查看器从上下文路 `Utils.js` 径加载的HTML5 SDK库( `/s7viewers` 所谓的统一SDK `include`)。 原因在于，查看器的逻辑可 `Utils.js` 以完全管理或类似运行时查看器库的位置，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的 `includes` 辅助查看器。
>
>
>因此，在页面上直接引用查看器使用的任 `include` 何辅助JavaScript会在将来部署新产品版本时破坏查看器功能。

1. 定义容器 `DIV`。

   将空元 `DIV` 素添加到要显示查看器的页面。 元 `DIV` 素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符 `DIV` 是定位的元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`。

   要使全屏功能在Internet Explorer中正常工作，请确保DOM中没有其他元素的堆叠顺序高于占位符 `DIV`。

   以下是定义的占位符元素的示 `DIV` 例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 设置查看器大小

   可以通过以绝对单位声明顶级CSS类的查看器，或 `.s7video360viewer` 者使用修饰符来设置查看器的静态 `stagesize` 大小。

   您可以将大小调整直接放在HTML页面上，或放在自定义查看器CSS文件中，该文件稍后会分配给AEM资产中的查看器预设记录——按需要，或使用命令显式传递 `style` 大小。

   有关 [使用CSS设置查看器样式的更多信息](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) ，请参阅自定义Video360查看器。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM资 `stagesize` 产的查看器预设记录中设置修改量——按需。 或者，您可以将查看器初始化代码与集合显式传递 `params` ，或作为“命令参考”部分中所述的API调用传递，如下所示：

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建类的一个实例，将所有配置信息传递给它的构造函数，并对查看器实例调 `s7viewers.Video360Viewer``init()` 用方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应包含字段， `containerId` 其中包含查看器容器ID的名称以及查看器支持的配置参数的嵌套 `params` JSON对象。

   在这种情况下，对 `params` 象必须至少将图像服务URL作为属性传递， `serverUrl` 并将初始资产作为参 `asset` 数。 通过基于JSON的初始化API，您可以创建查看器并将其开始为单行代码、作为属性传递的视频服务器URL、作为参数的初始资 `videoserverurl` 产以及作为属性的交互式数 `asset``interactivedata` 据。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码能够按其ID找到容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为获得最大兼容性，请 `init()` 在结束标签之前或在正 `BODY` 文事件上调用方 `onload()` 法。

   同时，容器元素不一定是网页布局的一部分。 例如，可能会使用分配给它的样 `display:none` 式来隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例的示例，将最小必要的配置选项传递给构造函数并调用方 `init()` 法。 该示例假定：

   * 查看器实例为 `video360Viewer`。
   * 占位符的名称 `DIV` 为 `s7viewer`。
   * 图像服务URL为 `https://s7d9.scene7.com/is/image`。
   * 视频服务器URL为 `https://s7d9.scene7.com/is/content`。
   * 资产是 `Viewers/space_station_360-AVS`。

   ```
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是一个简单网页的完整示例，该网页嵌入了具有固定大小的Video360查看器：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，它决定了查看器容器的运行时大小 `DIV`。 在以下示例中，假定网页允许查看者的容器占Web浏览器窗口大小的40%, `DIV` 同时保持其高度不受限制。 网页HTML代码如下所示：

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

将查看器添加到此类页面与固定大小嵌入的步骤类似。 唯一的区别是您无需显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入相同。 将容器DIV添加到现有 `"holder"` DIV。 以下代码是一个完整的示例。 请注意调整浏览器大小时查看器大小的更改方式，以及查看器长宽比与资产的匹配方式。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**定义宽度和高度的响应式嵌入**

如果定义了宽度和高度的响应式嵌入，则网页样式会有所不同。 它为DIV提供两种大小， `"holder"` 并将其放在浏览器窗口的中心。 此外，网页会将元素和元素的大 `HTML` 小设 `BODY` 置为100%。

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

其余的嵌入步骤与无限制高度的响应式嵌入步骤相同。 结果示例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会使用任何参数，并且配置参数是使用 `setContainerId()`、 `setParam()`和 `setAsset()` API方法指定的，这些方法具有单独的JavaScript调用。

以下示例说明如何将固定大小嵌入与基于setter的API结合使用：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```

