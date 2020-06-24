---
description: 交互式视频查看器是播放以H.264格式编码的流式和渐进式视频的视频播放器。
seo-description: 交互式视频查看器是播放以H.264格式编码的流式和渐进式视频的视频播放器。
seo-title: 交互式视频
solution: Experience Manager
title: 交互式视频
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2243'
ht-degree: 0%

---


# 交互式视频{#interactive-video}

交互式视频查看器是播放以H.264格式编码的流式和渐进式视频的视频播放器。

查看器还在视频内容旁边显示交互式产品色板。 同时支持单个视频和自适应视频集。 它设计为可在支持HTML5视频的桌面和移动Web浏览器上使用。 查看器支持视频内容顶部显示的可选隐藏式字幕、视频章节导航和社交共享工具。 此查看器旨在帮助您实现“购物视频”体验。 即，用户可以选择与特定视频时间区域关联的样本，并被重定向到客户网站上的快速视图或产品详细信息页面。

查看器类型为510。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

和

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参 [阅系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用交互式视频查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

交互式视频查看器表示主JavaScript文件和一组帮助文件（单个JavaScript包含在该特定查看器、资源和CSS使用的所有查看器SDK组件中），这些文件由查看器在运行时下载。

交互式视频查看器可在弹出模式下使用，它使用随图像服务查看器提供的生产就绪型HTML页。 它还可以在嵌入式模式下使用，在该模式下，它使用文档化的API集成到目标网页中。

配置和外观与本指南中介绍的其他查看器的配置和外观相似。 所有外观设计都通过自定义(CSS)层叠样式表实现。

请参 [阅所有查看器的通用命令参考——所有查看器](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[的通用配置属性和通用命令参考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与交互式视频查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

交互式视频查看器为视频播放提供了一套标准用户界面控件，如播放／暂停按钮、视频浏览条、视频时间气泡、播放时间／总时间指示器、音量控制、全屏按钮和隐藏字幕切换。 所有这些控件都直接组合到主视图下的控件条中。

请注意，在触控设备上，卷控件在用户界面中是隐藏的，因为只能使用设备的硬件按钮来控制卷。

当查看器在弹出模式下运行时，用户界面中不提供全屏按钮。

查看器在视频查看区域右侧显示一个包含交互式色板的面板。 播放视频时，色板的列表会自动前进，因此会显示与当前视频区域对应的色板。 单击或点按色板会触发在创作期间与此样板关联的操作。 根据设置方式，触发器可能会重定向到网站上的其他页面，或将产品信息传递回网页逻辑，而网页逻辑又会触发显示相关产品内容的快速视图的打开。

激活视频分页时，可以快速浏览视频内容。 视频章节在视频浏览条轨道中显示为标记，并在滚动时（或在触控系统上点击一下鼠标）显示章节标题和说明。 客户可以通过单击章节标记或点击章节描述气泡来“查找”特定章节。

查看器还支持各种社交媒体共享工具。 用户界面中的单个按钮可用，当用户单击或点击该按钮时，该按钮将扩展为共享工具栏。 共享工具栏包含支持的每种类型的共享渠道的图标，如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个带有相应数据输入表单的模态对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频播放会自动暂停。 共享工具在全屏模式下不可用，因为Web浏览器安全限制。

查看器完全可通过键盘访问。 请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入交互式视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

交互式视频查看器设计为嵌入到托管页面中。 此类网页可能具有静态布局，或者它可能是“响应式”的，并在不同设备或不同浏览器窗口大小下以不同方式显示。

为满足这些需求，查看器支持两种主要操作模式： 固定大小嵌入和响应式嵌入。

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常只占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，将使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器的大小变化 `DIV`。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式取决于网页调整其容器的方式 `DIV`。 如果网页仅设置容器的宽度，而 `DIV`保持高度不受限制，则查看器会根据所使用的资产的长宽比自动选择其高度。 此功能可确保资产完美地适合视图，而不会在两侧添加任何边距。 此用例是使用响应式Web设计布局框架(如Bootstrap、基础等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器的宽度和高度，则查看器仅填充该区域 `DIV`，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模态叠加中，其中叠加根据Web浏览器窗口大小进行大小调整。

**固定大小嵌入**

通过执行以下操作，可将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含该查看器 [!DNL InterativeVideoViewer.js]。 文 [!DNL InteractiveVideoViewer.js] 件位于标准IS [!DNL html5/js/] 查看器部署的子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果查看器部署在某个AdobeDynamic Media经典服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装了IS-Viewer的AdobeDynamic Media经典服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主 `include` 查看器JavaScript文件。 在网页代码中不应引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 尤其不要直接引用查看器从上 `Utils.js` 下文路径加载的 `/s7viewers` HTML5 SDK库(所谓的统一SDK `include`)。 原因在于查看器的逻辑 `Utils.js` 完全管理或类似运行时查看器库的位置，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的 `includes` 辅助查看器。
>
>
>因此，在页面上直接引用查看器使 `include` 用的任何辅助JavaScript会在将来部署新产品版本时破坏查看器功能。

1. 定义容器 `DIV`。

   向要显示 `DIV` 查看器的页面添加空元素。 元 `DIV` 素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符 `DIV` 是定位的元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`。

   要使全屏功能在Internet Explorer中正常工作，请确保DOM中没有其他元素的堆叠顺序高于占位符 `DIV`。

   以下是定义的占位符元素的 `DIV` 示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   您可以通过以绝对单位声明顶级CSS类的 `.s7interactivevideoviewer` 静态大小或使用修饰符来设置查看器的静 `stagesize` 态大小。

   您可以将大小调整直接放在HTML页面或自定义查看器CSS文件中，该文件稍后会以AEM Assets形式分配给查看器预设记录——按需要，或使用命令显式传 `style` 递。

   有关 [使用CSS设置查看器样式](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) ，请参阅自定义交互式视频查看器。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以在查看 `stagesize` 器预设记录中按需设置AEM Assets。 或者，可以将查看器初始化代码与集合 `params` 显式传递，或作为“命令参考”部分中所述的API调用，如下所示：

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建类的一个实例，将 `s7viewers.InteractiveVideoViewer` 所有配置信息传递给它的构造函数，并对查看器实例 `init()` 调用方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应包含 `containerId` 包含查看器容器ID名称的字段和嵌套JSON对象( `params` 查看器支持配置参数)。

   在这种情况下，对 `params` 象必须至少将图像服务URL作为属性传 `serverUrl` 递，并将初始资产作为 `asset` 参数。 基于JSON的初始化API允许您使用单行代码、作为属性传递的视频服务器URL、作为参数的初始资 `videoserverurl` 产以及作为属性的 `asset` 交互式数据创建和 `interactivedata` 开始查看器。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码能够按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为获得最大兼容性， `init()` 请在结束标签之前或 `BODY` 在正文事件上调用方 `onload()` 法。

   同时，容器元素不一定是网页布局的一部分。 例如，使用分配给它的样 `display:none` 式可能会隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 此时，查看器加载会自动恢复。

   以下是创建查看器实例的示例，将最小必要配置选项传递给构造函数并调用方 `init()` 法。 该示例假定：

   * 查看器实例为 `interactiveVideoViewer`。
   * 占位符的名称 `DIV` 为 `s7viewer`。
   * 图像服务URL为 `https://aodmarketingna.assetsadobe.com/is/image/`。
   * 视频服务器URL为 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`。
   * 内容URL为 `https://aodmarketingna.assetsadobe.com/`。
   * 资产是 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`。
   * 交互数据是 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`。

   ```
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

   以下代码是嵌入具有固定大小的交互式视频查看器的次要网页的完整示例：

   ```
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

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，这些布局决定了查看器容器的运行时大小 `DIV`。 在以下示例中，假定网页允许查看者的容器占Web浏 `DIV` 览器窗口大小的40%，同时保持其高度不受限制。 网页HTML代码如下所示：

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

上述所有步骤与固定大小嵌入相同。 将容器DIV添加到现有 `"holder"` DIV。 下面的代码是一个完整的示例。 注意调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```
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

以下示例页面说明了在不限制高度的情况下响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**定义了宽度和高度的响应式嵌入**

如果定义了宽度和高度的响应式嵌入，则网页样式会有所不同。 它为DIV提供两种大 `"holder"` 小，并将其居中在浏览器窗口中。 此外，网页会将元素和元素的 `HTML` 大小 `BODY` 设置为100%。

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

其余的嵌入步骤与无限制高度的响应式嵌入步骤完全相同。 结果示例如下：

```
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

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和无目标构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会使用任何参数，并且配置参数是使 `setContainerId()`用、 `setParam()`和API `setAsset()` 方法用单独的JavaScript调用指定的。

以下示例说明如何将固定大小嵌入与基于setter的API结合使用：

```
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

