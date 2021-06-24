---
description: HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码的流式和渐进式360视频，这些视频从Dynamic Media Classic或AEM Dynamic Media提供。
solution: Experience Manager
title: Video360
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,Business Practitioner
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码的流式和渐进式360视频，该视频从Dynamic Media Classic或AEM Dynamic Media提供。

360度视频，也称为沉浸式视频或球形视频，是录像，在录像中，可以同时记录每个方向的视图，使用全方位摄像机或一组摄像机拍摄。 同时支持单个视频集和自适应视频集。 此外，查看器还支持使用在外部位置托管的渐进式视频流和HLS流。

360视频的推荐宽高比为2:1。 不支持空间声音。 该查看器设计为仅处理360个视频；尝试播放非360视频会导致视频播放失真。

查看器可同时在支持HTML5视频的桌面和移动Web浏览器上使用。 查看器支持可选的社交共享工具。

当基础系统支持HLS格式时，Video360查看器在其默认配置中使用HTML5流视频播放。 在不支持HTML5流播放的系统上，查看器会返回到HTML5渐进式视频交付。

查看器类型为517。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅[系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360查看器表示主JavaScript文件和一组帮助程序文件(单个JavaScript包含该查看器在运行时下载的特定查看器（资产、CSS）所使用的所有HTML5查看器SDK组件)。

HTML5 Video360查看器既可以在弹出模式下使用IS-Viewer提供的生产就绪HTML页面，也可以在嵌入式模式下使用，在这种模式下，查看器可以使用记录在案的API集成到目标网页中。

配置和外观设置与本指南中所述其他查看器的配置和外观设置类似。 所有外观设置均通过自定义(CSS)层叠样式表实现。

请参阅所有查看器的通用命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有查看器通用的命令引用 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[

360视频内容要求的编码设置比标准非360视频要高。 换句话说，360个内容必须比非360视频分辨率高，才能获得相同的可感知质量。 建议您为360视频考虑以下自适应视频预设设置：

* 720p，2500 kbps
* 1080p，5000 kbps
* 1440p，6600 kbps

但是，请注意，使用如此高质量设置编码的视频服务要求在最终用户设备上进行高带宽连接。

## 与Video360查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360查看器为视频播放提供了一组标准用户界面控件，如播放/暂停按钮、视频清理器视频时间气泡、播放时间/总时间指示器、音量控制和全屏按钮。 所有这些控件都分组到查看器用户界面最底部的控制栏中。

请注意，在触屏设备上，卷控件在用户界面中处于隐藏状态，因为只有使用设备的硬件按钮才能控制卷。

当查看器在弹出模式下运行时，用户界面中不提供全屏按钮。

查看器还支持各种社交媒体共享工具。 用户界面中的按钮可用作单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。 共享工具栏包含支持的每种类型共享渠道的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个包含相应数据输入表单的模式对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，在激活共享工具后，视频播放会自动暂停。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

该查看器支持在VR头戴设备（如Oculus Go和Oculus Rift）、VR HMD（头戴式显示器）安装（如Google Cardboard）和非VR启用设备（如桌面浏览器、平板电脑和未连接到VR HMD安装的手机）上播放360次视频。

在VR头戴式耳机上查看360个视频内容时，无需进行其他配置。 查看器会自动检测VR头戴式耳机的存在，并在视频内容的顶部显示“VR”按钮。 激活此“VR”按钮会将视频渲染切换为VR模式。 查看器仅支持在支持WebVR的浏览器中渲染VR。

要使用VR HMD安装，必须在查看器配置中将`Video360Player.vrrender`修饰符设置为`1`，这将强制进行立体渲染。

在VR耳机和VR HMD安装时，视点更改会因头戴式耳机移动而发生，而在VR模式下不提供其他播放控制。

在启用了VR的设备上观看360个视频时，最终用户可以使用鼠标、触摸或键盘来控制视频播放和视点。

在Windows设备上，查看器通过触摸屏和鼠标同时支持触摸输入和鼠标输入，但此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

查看器完全可通过键盘访问。 请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时，网页会提供一个链接，单击该链接后，查看者便会在单独的浏览器窗口中打开。 在其他情况下，需要将查看器直接嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 在大多数情况下，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频会自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户可以始终返回到该视频并继续播放。 唯一例外是，在Android 4.x设备上的Chrome浏览器中，这项规则可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向发生更改时进行调整。

此模式是移动设备最常使用的模式。 网页会使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议使用现成的HTML页面进行弹出操作模式。 它名为[!DNL Video360Viewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占据网页的一部分房地产。

主要用例包括面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式与网页大小其容器`DIV`的方式不同。 如果网页仅设置容器的宽度`DIV`，并且不限制其高度，则查看器会根据所使用资产的宽高比自动选择其高度。 此功能可确保资产完美地放入视图中，侧边无需任何内边距。 对于使用响应式Web设计布局框架(如Bootstrap、基础等)的网页，此用例最常见。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML标头中添加脚本标记。 在使用查看器API之前，请确保包含[!DNL Video360Viewer.js]。 [!DNL Video360Viewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果查看器部署在某个Adobe的Dynamic Media Classic服务器上，并且从同一域提供该查看器，则可以使用相对路径。 否则，您将指定一个安装IS-Viewer的AdobeDynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能会在运行时由查看器的逻辑下载。 特别是，切勿直接引用查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生更改。 Adobe不会在服务器上保留旧版次查看器`includes`。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时中断查看器功能。

1. 定义容器`DIV`。

   将空的`DIV`元素添加到您希望查看器显示的页面中。 必须定义`DIV`元素的ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符`DIV`是已定位的元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   要使全屏功能在Internet Explorer中正常运行，请确保DOM中没有其他元素的堆叠顺序比占位符`DIV`的堆叠顺序高。

   以下是定义的占位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 设置查看器大小

   您可以通过以下两种方式设置查看器的静态大小：以绝对单位声明查看器的`.s7video360viewer`顶级CSS类，或使用`stagesize`修饰符。

   您可以将大小调整直接放在HTML页面的CSS中，或放在自定义查看器CSS文件中，该文件稍后会分配给AEM Assets中的查看器预设记录 — 按需，或使用`style`命令显式传递。

   请参阅[自定义Video360查看器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) ，以了解有关使用CSS为查看器设置样式的更多信息。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM Assets的查看器预设记录中设置`stagesize`修饰符 — 按需。 或者，您也可以通过查看器初始化代码与`params`集合进行显式传递，或作为API调用（如命令引用部分中所述）进行传递，如下所示：

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   建议使用基于CSS的方法，该方法将在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个`s7viewers.Video360Viewer`类的实例，将所有配置信息传递给其构造函数，并在查看器实例中调用`init()`方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称，以及嵌套的`params` JSON对象，且该对象具有查看器支持的配置参数。

   在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为`asset`参数传递。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器，将视频服务器URL作为`videoserverurl`属性传递，将初始资产作为`asset`参数，将交互式数据作为`interactivedata`属性传递。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大的兼容性，请在结束`BODY`标记之前或在主体`onload()`事件上调用`init()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式来隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下示例用于创建一个查看器实例，将所需的最小配置选项传递给构造函数并调用`init()`方法。 该示例假定：

   * 查看器实例为`video360Viewer`。
   * 占位符`DIV`的名称为`s7viewer`。
   * 图像服务URL为`https://s7d9.scene7.com/is/image`。
   * 视频服务器URL为`https://s7d9.scene7.com/is/content`。
   * 资产为`Viewers/space_station_360-AVS`。

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

   以下代码是嵌入具有固定大小的Video360查看器的简单网页的完整示例：

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

**具有无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，指示查看器容器`DIV`的运行时大小。 对于以下示例，假定网页允许查看器的容器`DIV`占用Web浏览器窗口大小的40%，并保持其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面的步骤与固定大小嵌入的步骤类似。 唯一的区别在于您无需明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同。 将容器DIV添加到现有的`"holder"` DIV中。 以下代码是一个完整的示例。 请注意在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

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

**定义了宽度和高度的响应式嵌入**

在定义了宽度和高度的响应式嵌入时，网页样式会有所不同。 它为`"holder"` DIV提供两种大小，并将其放在浏览器窗口的中心。 此外，该网页还会将`HTML`和`BODY`元素的大小设置为100%。

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

其余嵌入步骤与无限制高度的响应嵌入步骤相同。 结果示例如下：

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

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会获取任何参数，并且配置参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例说明了如何在基于setter的API中使用固定大小嵌入：

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
