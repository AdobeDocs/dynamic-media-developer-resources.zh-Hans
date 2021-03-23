---
description: HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码、从Dynamic Media Classic或AEM Dynamic Media提供的渐进式360流视频。
solution: Experience Manager
title: Video360
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2593'
ht-degree: 0%

---


# Video360{#video}

HTML5 Video360查看器是一个360度视频播放器，可播放以H.264格式编码、从Dynamic Media Classic或AEM Dynamic Media提供的渐进式360流视频。

360度视频，又称沉浸式视频或球形视频，是一些视频录制，在这些视频中，每个方向的视图都同时被录制，使用全向摄像机或一组摄像机拍摄。 同时支持单个视频和自适应视频集。 此外，查看器还支持使用在外部位置托管的渐进式视频和HLS流。

360视频的建议宽高比为2:1。 不支持空间音效。 查看器设计为仅用于360视频；尝试播放非360视频会导致视频播放失真。

查看器设计为可在支持HTML5视频的桌面和移动Web浏览器上使用。 查看器支持可选的社交共享工具。

当基础系统支持HLS格式时，Video360查看器在其默认配置中使用HTML5流视频播放。 在不支持HTML5流的系统上，查看器回退到HTML5渐进式视频投放。

查看器类型为517。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅[系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用Video360查看器{#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360查看器表示主JavaScript文件和一组帮助文件（单个JavaScript包含在由查看器在运行时下载的该特定查看器、资源、CSS使用的所有HTML5查看器SDK组件中）。

HTML5 Video360查看器既可以在弹出模式下使用，也可以在嵌入式模式下使用，即使用随IS-Viewer提供的生产就绪型HTML页面，或在嵌入式模式下使用文档化的API将其集成到目标网页中。

配置和外观设置与本指南中介绍的其他查看器类似。 所有外观设置均通过自定义(CSS)层叠样式表实现。

请参阅所有查看器的通用命令参考 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看器通用的通用命令参考 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[[

360视频内容要求的编码设置高于标准非360视频。 换句话说，360个内容必须比非360视频分辨率更高，才能实现相同的可感知质量。 建议您为360视频考虑以下自适应视频预设设置：

* 720p，2500 kbps
* 1080p，5000 kbps
* 1440p，6600 kbps

但是，请注意，提供使用这种高质量设置编码的视频需要在最终用户的设备上实现高带宽连接。

## 与Video360查看器交互{#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360查看器为视频播放提供了一套标准用户界面控件，如播放/暂停按钮、视频浏览器视频时间泡、播放时间/总时间指示器、音量控制和全屏按钮。 所有这些控件都分组到查看器用户界面底部的控制栏中。

请注意，在触控设备上，卷控件在用户界面中是隐藏的，因为只有使用设备的硬件按钮才能控制卷。

查看器在弹出模式下操作时，用户界面中不提供全屏按钮。

查看器还支持各种社交媒体共享工具。 用户界面中的单个按钮可用，当用户单击或点按时，该按钮将扩展为共享工具栏。 共享工具栏包含支持的每种类型的共享渠道的图标，如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个带有相应数据输入表单的模态对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频播放会自动暂停。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

查看器支持在VR头盔（如Oculus Go和Oculus Rift）、VR HMD（头戴式显示屏）安装（如Google Cardboard）和非VR启用设备（如桌面浏览器、平板电脑和未连接到VR HMD安装的手机）上播放360个视频。

在VR头戴式耳机上视图360视频内容无需额外配置。 查看器会自动检测是否存在VR头戴式耳机，并在视频内容顶部显示“VR”按钮。 激活此“VR”按钮会将视频渲染切换到VR模式。 查看器仅支持在具有WebVR支持的浏览器中进行VR渲染。

为了使用VR HMD安装，必须在查看器配置中将`Video360Player.vrrender`修饰符设置为`1`，这会强制进行立体渲染。

在VR耳机和VR HMD上，视图改变点响应于头戴式耳机移动而发生，而在VR模式中不提供其他回放控制。

当在未启用VR的设备上观看360视频时，最终用户可以使用鼠标、触摸或键盘控制视频播放和视图点。

查看器支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入，但仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

查看器完全可通过键盘访问。 请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入Video360查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看器行为有不同的需求。 有时，网页会提供链接，单击该链接后，查看器将在单独的浏览器窗口中打开。 在其他情况下，必须将查看器直接嵌入到托管页面。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同的内容，或针对不同的浏览器窗口大小显示不同的内容。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 在大多数情况下，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，会自动暂停第一个视频。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回并继续播放。 此规则的唯一例外是Android 4.x设备上的Chrome浏览器，它可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式是移动设备最常见的模式。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 它名为[!DNL Video360Viewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以通过应用自定义CSS实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常仅占据网页的一部分空间。

主要用例是面向桌面或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 对于具有静态布局的网页，这是最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页大小其容器`DIV`的方式而异。 如果网页仅设置容器的宽度`DIV`，而保持高度不受限，则查看器会根据所使用资产的宽高比自动选择其高度。 此功能可确保资产完美适合视图，且两侧无填充。 此用例是使用响应式Web设计布局框架(如Bootstrap、Foundation等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个不错的示例是将查看器嵌入到模式叠加中，其中的叠加会根据Web浏览器窗口大小进行调整。

**固定大小嵌入**

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标签。 在使用查看器API之前，请确保包含[!DNL Video360Viewer.js]。 [!DNL Video360Viewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并从同一域提供，则可以使用相对路径。 否则，您将指定一个指向安装了IS-Viewer的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用由查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是，`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生变化。 Adobe不会将旧版次查看器`includes`保留在服务器上。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时破坏查看器功能。

1. 定义容器`DIV`。

   在希望查看器显示的页面中添加空`DIV`元素。 `DIV`元素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符`DIV`是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   要使全屏功能在Internet Explorer中正常工作，请确保DOM中没有其他元素的堆叠顺序高于占位符`DIV`。

   以下是定义的占位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 设置查看器大小

   您可以通过以下两种方式设置查看器的静态大小：以绝对单位为`.s7video360viewer`顶级CSS类声明查看器，或使用`stagesize`修饰符。

   您可以将大小调整直接放在HTML页面或自定义查看器CSS文件中，该文件随后将分配给AEM Assets中的查看器预设记录 — 按需，或使用`style`命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义Video360查看器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页中定义静态查看器大小的示例：

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在AEM Assets的查看器预设记录中设置`stagesize`修饰符 — 按需。 或者，您可以将查看器初始化代码与`params`集合显式传递，或作为“命令参考”部分中所述的API调用进行传递，如下所示：

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建`s7viewers.Video360Viewer`类的实例，将所有配置信息传递给它的构造函数，并对查看器实例调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称以及查看器支持的配置参数嵌套的`params` JSON对象。

   在这种情况下，`params`对象必须至少具有作为`serverUrl`属性传递的图像服务URL，以及作为`asset`参数传递的初始资产。 基于JSON的初始化API允许您使用单行代码创建和开始查看器，将视频服务器URL作为`videoserverurl`属性传递，将初始资产作为`asset`参数，将交互式数据作为`interactivedata`属性。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会将构建DOM延迟到网页结束。 要获得最大兼容性，请在结束`BODY`标签之前或在正文`onload()`事件上调用`init()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可能会使用分配给它的`display:none`样式将其隐藏。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例的示例，将最小必要的配置选项传递给构造函数并调用`init()`方法。 该示例假定：

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

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，指示查看器容器的运行时大小`DIV`。 在以下示例中，假定网页允许查看器的容器`DIV`占Web浏览器窗口大小的40%，同时保持其高度不受限制。 网页HTML代码如下所示：

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

上述步骤与固定大小嵌入相同。 将容器DIV添加到现有`"holder"` DIV。 以下代码是一个完整的示例。 请注意，调整浏览器大小时查看器大小的更改方式，以及查看器长宽比与资产的匹配方式。

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

如果定义了宽度和高度的响应式嵌入，则网页样式会有所不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页会将`HTML`和`BODY`元素的大小设置为100%。

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

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会使用任何参数和配置参数，这些参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

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

