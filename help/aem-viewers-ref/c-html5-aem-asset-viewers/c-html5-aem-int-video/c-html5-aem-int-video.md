---
title: 交互式视频
description: 交互式视频查看器是一种视频播放器，可播放以H.264格式编码的流视频和渐进视频。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# 交互式视频{#interactive-video}

交互式视频查看器是一种视频播放器，可播放以H.264格式编码的流视频和渐进视频。

查看器还会在视频内容旁边显示交互式产品样本。 支持单个视频和自适应视频集。 它设计为可在支持HTML5视频的桌面和移动Web浏览器上工作。 查看器支持在视频内容、视频章节导航和社交共享工具顶部显示的可选隐藏字幕。 此查看器旨在帮助您实施“可购物视频”体验。 即，用户可以选择与特定视频时间区域关联的色板，并重定向到客户网站上的概览或产品详细信息页面。

查看器类型为510。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html?lang=zh-Hans)

和

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html?lang=zh-Hans)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅[系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用交互式视频查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

交互式视频查看器表示主JavaScript文件以及查看器在运行时下载的一组帮助程序文件。 单个JavaScript包含在此特定查看器、资源和CSS使用的所有查看器SDK组件中。

交互式视频查看器可在弹出模式下使用，具体方式是使用随图像服务查看器提供的生产就绪的HTML页面。 它还可以在嵌入模式下使用，在该模式下，使用文档记录的API将其集成到目标网页中。

配置和外观设计类似于本指南中描述的其他查看器的配置和外观。 所有外观设计都是通过自定义(CSS)层叠样式表实现的。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与交互式视频查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

交互式视频查看器提供一组用于视频播放的标准用户界面控件，如播放/暂停按钮、视频洗刷器、视频时间气泡、播放时间/总时间指示器、音量控件、全屏按钮和隐藏式字幕切换开关。 所有这些控件都分组到主视图下的控件栏中。

在触控设备上，音量控制对用户界面是隐藏的，因为只能使用设备的硬件按钮来控制音量。

当查看器以弹出模式运行时，全屏按钮在用户界面中不可用。

查看器会在视频查看区域的右侧显示一个带有交互式样本的面板。 样本列表会在视频播放时自动前进，以便显示对应于当前视频区域的样本。 单击或点按样本会触发在创作期间与此类样本关联的操作。 根据您的设置方式，触发器可能会重定向到网站上的其他页面。 或者，它可能会将产品信息传递回网页逻辑，从而触发显示相关产品内容的概览打开。

在激活视频章节时，可以快速导航视频内容。 视频章节将作为标记显示在视频洗刷跟踪中，并在变换图像（或在触摸系统上单点按）时显示章节标题和描述。 客户可以通过单击章节标记或点按章节描述气泡“搜寻”特定章节。

查看器还支持各种社交媒体共享工具。 它们可用作用户界面中的单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。 共享工具栏中包含有关支持的每种共享渠道类型的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个模式对话框，其中包含相应的数据输入表单。 在调用Facebook或Twitter时，查看者会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具激活时，视频播放会自动暂停。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

查看器完全可使用键盘。 请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入交互式视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

交互式视频查看器将嵌入到托管页面中。 这样的网页可以具有静态布局，或者它可以“响应式”并且在不同设备或不同浏览器窗口大小上以不同的方式显示。

为了满足这些需求，查看器支持两种主要操作模式：固定大小嵌入和响应式嵌入。

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 此功能是拥有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器需要在运行时调整大小以响应其容器`DIV`的大小更改。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页调整其容器`DIV`大小的方式。 如果网页仅设置容器`DIV`的宽度，而不限制其高度，则查看器会根据所用资源的长宽比自动选择其高度。 此功能可确保资产完全适合视图，不会出现任何边距。 此用例最常用于使用响应式Web设计布局框架(如Bootstrap和Foundation)的网页。

否则，如果网页同时设置了查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括[!DNL InterativeVideoViewer.js]。 [!DNL InteractiveVideoViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>仅引用页面上的主查看器JavaScript `include`文件。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，请勿直接引用查看器从`Utils.js`上下文路径(所谓的统一HTML `/s7viewers`)加载的SDK5 SDK `include`库。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的辅助查看器`includes`。
>
>
>因此，将来在部署新产品版本时，在页面上直接引用查看器使用的任何二级JavaScript `include`会破坏查看器功能。

1. 正在定义容器`DIV`。

   向您希望查看器显示的页面添加一个空`DIV`元素。 `DIV`元素必须定义其ID，因为此ID稍后将传递到查看器API。 DIV的大小通过CSS指定。

   占位符`DIV`是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   要使全屏功能在Internet Explorer中正常运行，请确保DOM中没有其他元素的栈叠顺序高于占位符`DIV`。

   以下是定义的占位符`DIV`元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   您可以通过声明查看器为`.s7interactivevideoviewer`顶级CSS类（以绝对单位表示）或使用`stagesize`修饰符来设置查看器的静态大小。

   您可以在HTML页面上直接放置在CSS中的大小。 或者，您可以将其放入自定义查看器CSS文件中，稍后将该文件分配给Adobe Experience Manager Assets中的查看器预设记录（按需），或使用`style`命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义交互式视频查看器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在Experience Manager Assets的查看器预设记录中设置`stagesize`修饰符 — 按需。 或者，您也可以使用`params`集合的查看器初始化代码显式传递它，或作为API调用传递，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.InteractiveVideoViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段保存查看器容器ID的名称，并使用查看器支持的配置参数嵌套`params` JSON对象。

   在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为`asset`参数传递。 基于JSON的初始化API允许您使用一行代码、作为`videoserverurl`属性传递的视频服务器URL、作为`asset`参数的初始资产以及作为`interactivedata`属性的交互式数据来创建和启动查看器。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 之后，查看器加载会自动继续。

   以下示例用于创建查看器实例，将所需的最少配置选项传递给构造函数并调用`init()`方法。 此示例假设以下内容：

   * 查看器实例为`interactiveVideoViewer`。
   * 占位符`DIV`的名称为`s7viewer`。
   * 图像服务URL为`https://aodmarketingna.assetsadobe.com/is/image/`。
   * 视频服务器URL为`https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 内容URL为`https://aodmarketingna.assetsadobe.com/`。
   * 资产为`/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 交互式数据为`is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是一个简单网页的完整示例，该网页以固定大小嵌入交互式视频查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器`DIV`的运行时大小。 对于以下示例，假设网页允许查看者的容器`DIV`占用Web浏览器窗口大小的40%，并且其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与嵌入固定大小的步骤类似。 唯一的区别是，您不需要显式定义查看器大小。

1. 正在将查看器JavaScript文件添加到您的网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 将容器DIV添加到现有`"holder"` DIV。 以下代码是一个完整的示例。 请注意当浏览器调整大小时查看器大小如何变化，以及查看器长宽比如何与资源匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hans)

定义宽度和高度的&#x200B;**响应式嵌入**

如果有定义了宽度和高度的响应式嵌入，则网页样式会不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%。

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

其余嵌入步骤与用于高度不受限制的响应式嵌入的步骤相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会接受任何参数，配置参数是使用`setContainerId()`、`setParam()`和`setAsset()` API方法通过单独的JavaScript调用指定的。

以下示例说明了如何将固定大小嵌入与基于setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
