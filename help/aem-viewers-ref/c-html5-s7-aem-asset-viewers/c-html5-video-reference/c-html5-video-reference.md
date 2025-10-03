---
title: 视频
description: 视频查看器是一种视频播放器，可播放以H.264格式编码的流视频和渐进视频。 它通过Dynamic Media从Dynamic Media Classic或Adobe Experience Manager提供。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2329'
ht-degree: 0%

---

# 视频{#video}

视频查看器是一种视频播放器，可播放以H.264格式编码的流视频和渐进视频。 它通过Dynamic Media从Dynamic Media Classic或Experience Manager提供。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

支持单个视频和自适应视频集。 此外，查看器支持使用托管在外部位置的渐进式视频流和HLS流。 它设计为可在支持HTML5视频的桌面和移动Web浏览器上工作。 此查看器还支持在视频内容、视频章节导航和社交媒体共享工具顶部显示的可选隐藏式字幕。

只要底层系统支持，视频查看器就会在其默认配置中使用HLS格式的HTML5流视频播放。 在不支持HTML5流传输的系统上，查看器回退到HTML5渐进式视频交付。

查看器类型506。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 使用视频查看器 {#section-f21ac23d3f6449ad9765588d69584772}

视频查看器表示一个主JavaScript文件和一组帮助程序文件 — 单个JavaScript包含此特定查看器使用的所有Viewer SDK组件、资源以及查看器在运行时下载的CSS。

您可以使用随IS-Viewer提供的生产就绪型HTML页面在弹出模式下使用视频查看器。 或者，您可以在嵌入模式下使用查看器，在该模式下，使用文档记录的API将其集成到目标网页中。

配置查看器和为其设置外观的任务与其他查看器的任务类似。 所有外观设计都是通过自定义CSS实现的。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与视频查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

视频查看器提供一组用于视频播放的标准用户界面控件，如播放/暂停按钮、视频洗刷视频时间气泡、播放时间/总时间指示器、音量控件、全屏按钮和隐藏式字幕切换。 所有这些控件都分组到查看器用户界面底部的控件栏中。

在触控设备上，音量控制对用户界面是隐藏的，因为只能使用硬件按钮控制音量。

当查看器以弹出模式运行时，全屏按钮在用户界面中不可用。

在激活视频章节时，可以快速导航视频内容。 视频章节将作为标记显示在视频洗刷轨道中，并在鼠标滚动或点按触摸系统时显示章节标题和相关描述。 用户可以通过选择章节标记或选择章节描述气泡来查找特定章节。

该查看器支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用视频查看器共享社交媒体工具 {#section-907d316fe1da4b87abb9775f02464704}

视频查看器支持社交媒体共享工具。 它们可用作用户界面中的单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏中包含有关支持的每种共享渠道类型的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个模式对话框，其中包含相应的数据输入表单。 在调用Facebook或Twitter时，查看者会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频播放也会自动暂停。

由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供一个链接，选中该链接后，查看器将在单独的浏览器窗口中打开。 在其他情况下，需要直接将查看器嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同的设备上或对于不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 通常，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回并继续播放。 此规则唯一的例外是在Android™ 4.x设备上的Chrome浏览器中，该浏览器可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式最适用于移动设备。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您为弹出窗口操作模式使用现成的HTML页面。 它名为[!DNL VideoViewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器`DIV`的大小更改。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页调整其容器`DIV`大小的方式。 如果网页仅设置容器`DIV`的宽度，而不限制其高度，则查看器会根据所用资源的长宽比自动选择其高度。 此方法可确保资产完全适合视图，而不会在两侧添加任何边距。 此用例最常见于使用响应式设计布局框架(如Bootstrap或基础)的网页。

否则，如果网页同时设置了查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口的大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括[!DNL FlyoutViewer.js]。 [!DNL FlyoutViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>仅引用页面上的主查看器JavaScript `include`文件。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，请勿直接引用查看器从`Utils.js`上下文路径(所谓的统一HTML `/s7viewers`)加载的SDK5 SDK `include`库。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的辅助查看器`includes`。
>
>
>因此，将来在部署新产品版本时，在页面上直接引用查看器使用的任何二级JavaScript `include`会破坏查看器功能。

1. 定义容器DIV。

   向要显示查看器的页面添加一个空DIV元素。 DIV元素必须定义其ID，因为此ID稍后将传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   确保全屏功能在Internet Explorer中正常工作。 检查以确保DOM中没有其他元素的栈叠顺序高于占位符DIV。

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 设置查看器大小

   可以通过以绝对单位为`.s7videoviewer`顶级CSS类声明查看器静态大小，也可以使用修饰符`stagesize`来设置查看器的静态大小。

   您可以在HTML页面或自定义查看器CSS文件中直接在CSS中放置大小。 之后，会将该配置文件分配给Dynamic Media Classic中的查看器预设记录，或者使用样式命令显式传递配置文件。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义视频查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic中的查看器预设记录中设置`stagesize`修饰符，或通过`params`集合显式传递查看器初始化代码。 或者，作为API调用，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.VideoViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段保存查看器容器ID的名称，并嵌套`params` JSON对象，其中包含查看器支持的配置参数。 在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，将视频服务器URL作为`videoserverurl`属性传递，并将初始资产作为`asset`参数传递。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载将自动继续。

   以下示例用于创建查看器实例、将最低必要的配置选项传递给构造函数以及调用`init()`方法。 此示例假定`videoViewer`是查看器实例，`s7viewer`是占位符`DIV`的名称，[!DNL http://s7d1.scene7.com/is/image/]是图像服务URL，[!DNL http://s7d1.scene7.com/is/content/]是视频服务器URL，[!DNL Scene7SharedAssets/Glacier_Climber_MP4]是资产。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   以下代码是一个简单网页的完整示例，该网页以固定大小嵌入视频查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器`DIV`的运行时大小。 对于此示例，假设网页允许查看者的容器`DIV`占用Web浏览器窗口大小的40%，并且其高度不受限制。 网页HTML代码如下所示：

```html {.line-numbers}
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

将查看器添加到此类页面与嵌入固定大小类似；唯一的区别是无需明确定义查看器大小。

1. 正在将查看器JavaScript文件添加到您的网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 将容器`DIV`添加到现有“持有者”`DIV`。 以下代码是一个完整的示例。 您可以查看在调整浏览器大小时查看器大小的变化情况，以及查看器纵横比与资源的匹配情况。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下示例页面说明了如何更真实地使用高度不受限制的响应式设计嵌入：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

-->

**定义了宽度和高度的响应式设计嵌入**

如果有定义了宽度和高度的响应式设计嵌入，则网页样式将不同；它为“所有者” `DIV`提供大小，并将其居中在浏览器窗口中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%：

```html {.line-numbers}
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

其余嵌入步骤与高度不受限制的响应式设计嵌入相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 在该API中，构造函数不接受任何参数，并且配置参数是使用具有单独的JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例说明了使用基于setter的API嵌入固定大小：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
