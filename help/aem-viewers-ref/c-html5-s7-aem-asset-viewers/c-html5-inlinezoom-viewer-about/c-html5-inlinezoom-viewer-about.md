---
title: 内联缩放
description: 内联缩放查看器是一个图像查看器。 当用户滑过或触摸主视图时，它会显示一个静态图像，该静态图像上会显示缩放后的版本。 此查看器适用于图像集，并且使用样本完成导航。 它设计为可在台式机和移动设备上工作。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# 内联缩放{#inline-zoom}

内联缩放查看器是一个图像查看器。 当用户滑过或触摸主视图时，它会显示一个静态图像，该静态图像上会显示缩放后的版本。 此查看器适用于图像集，并且使用样本完成导航。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型为504。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&stagesize=500,400)

## 使用内联缩放查看器 {#section-f21ac23d3f6449ad9765588d69584772}

内联缩放查看器表示一个主JavaScript文件和一组帮助程序文件(单个JavaScript包含此特定查看器使用的所有SDK组件、资源、CSS)，这些文件由查看器在运行时下载。

嵌入式缩放查看器既可用于使用随图像服务查看器提供的生产就绪型HTML页面的弹出模式，也可用于使用文档化API将其集成到目标网页的嵌入模式。

其配置和外观设计与其他查看器的配置和外观设计类似。 您可以使用自定义CSS来应用外观设置。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与内联缩放查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

内联缩放查看器支持在其他移动设备应用程序中常见的单点触控和多点触控手势。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手势 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>单点按 </p> </td> 
   <td colname="col2"> <p> 激活弹出视图或在样本中的主缩放级别和次缩放级别之间更改，选择新缩略图。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 在样本栏中滚动样本列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫 </p> </td> 
   <td colname="col2"> <p>如果该手势在样本区域内完成，则会执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

该查看器还支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入内联缩放查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供可单击的链接，该链接会在单独的浏览器窗口中打开查看器。 在其他情况下，可能需要将查看器直接嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用在不同设备上显示不同或者用于不同浏览器窗口大小的响应式设计。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式嵌入。

**弹出窗口**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器窗口调整大小或设备方向更改时进行调整。

此模式最适用于移动设备。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方式加载查看器。

建议您将现成的HTML页面用于名为`FlyoutViewer.html`的弹出模式。 它位于标准图像服务查看器部署的[!DNL html5/]子文件夹下：

`<s7viewers_root>/html5/FlyoutViewer.html`

还必须将FlyoutZoomView组件配置为以内联缩放模式工作。 建议为内联缩放查看器使用现成的`Scene7SharedAssets/Universal_HTML5_Zoom_Inline`预设，或者使用从中派生的自定义预设。 可以通过应用自定义CSS来实现可视化自定义。

以下是一个HTML代码示例，它会在新窗口中打开查看器：

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定大小嵌入和响应式嵌入**

在嵌入式模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 观看者通常只占用网页的一部分空间。

主要用例是面向桌面或平板电脑设备的网页，以及根据设备类型自动调整布局的响应网页。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入模式。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入模式假定查看器必须在运行时调整大小以响应其容器`DIV`的大小更改。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

将响应式设计嵌入模式与内联缩放查看器结合使用时，请确保使用`imagereload`参数为主视图图像指定显式断点。 理想情况下，将断点与网页CSS指令的查看器宽度断点相匹配。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页容器`DIV`的大小方式。 如果网页仅设置容器`DIV`的宽度，而不限制其高度，则查看器会根据所用资源的长宽比自动选择其高度。 这项功能意味着资产可以完美地融入视图中，而不会有任何边距。 此特定用例最常见于使用响应式设计布局框架(如Bootstrap或基础)的网页。

否则，如果网页同时设置了查看器容器`DIV`的宽度和高度，则查看器将仅填充该区域，并遵循网页布局提供的大小。 一个良好的用例示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括`FlyoutViewer.js`。 `FlyoutViewer.js`在标准IS-Viewers部署的以下[!DNL html5/js/]子文件夹中：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在某个Adobe Dynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，您可以指定已安装IS-Viewers的某个Adobe Dynamic Media服务器的完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>仅引用页面上的主查看器JavaScript `include`文件。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，请勿直接引用查看器从`Utils.js`上下文路径(所谓的统一HTML `/s7viewers`)加载的SDK5 SDK `include`库。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的辅助查看器`includes`。
>
>
>因此，将来在部署新产品版本时，在页面上直接引用查看器使用的任何二级JavaScript `include`会破坏查看器功能。

1. 定义容器DIV。

   向要显示查看器的页面添加一个空DIV元素。 DIV元素必须定义其ID，因为此ID稍后将传递到查看器API。

   占位符DIV是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   网页负责为占位符DIV元素指定适当的`z-index`。 这样做可确保查看器的弹出部分显示在其他网页元素的上方。

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图。 在桌面系统上，缩览图位于主视图的下方。 同时，查看器允许在运行时使用`setAsset()` API交换主资源。 作为开发人员，当新资产只有一个项目时，您可以控制查看器管理底部区域中缩略图区域的方式。 可以保持外部查看器大小不变，并允许主视图增加其高度并占据缩略图区域。 或者，您可以保持主视图大小为静态并折叠外部查看器区域，让网页内容向上移动，然后使用缩略图中的剩余自由页面区域。

   要保持外部查看器边界不变，请定义`.s7flyoutviewer`顶级CSS类的大小（以绝对单位表示）。 CSS的大小调整可直接放在HTML页面或自定义查看器CSS文件中，稍后再分配给Dynamic Media Classic中的查看器预设记录，或使用style命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义内联缩放查看器](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451)。

   以下是在HTML页面中定义静态外部查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下面的示例页面上看到带有固定外部查看器区域的行为。 请注意，在组之间切换时，外部查看器大小不会更改：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html?lang=zh-Hans)

   要使主视图维度为静态维度，请使用`Container` CSS选择器为内部`.s7flyoutviewer .s7container` SDK组件定义查看器大小（以绝对单位表示）。 此外，您应将默认查看器CSS设置为`.s7flyoutviewer`，以覆盖为`auto`顶级CSS类定义的固定大小。

   下面是一个示例，用于为内部`Container` SDK组件定义查看器大小，以便在切换资源时主视图区域不会更改其大小：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下示例页面显示了固定主视图大小的查看器行为。 请注意，在页面集之间切换时，主视图将保持静态状态，网页内容将垂直移动：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html?lang=zh-Hans)

   此外，默认查看器CSS为开箱即用的外部区域提供固定大小。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.FlyoutViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称，并嵌套`params` JSON对象以及查看器支持的配置参数。 在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递；将初始资产作为`asset`参数，将CSS作为`contentUrl`参数加载的基本路径以及预设名称作为`config`参数。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 进行此操作后，查看器加载会自动恢复。

   以下示例用于创建查看器实例，将所需的最少配置选项传递给构造函数并调用`init()`方法。 该示例假设`inlineZoomViewer`是查看器实例；`s7viewer`是占位符`DIV`的名称；`http://s7d1.scene7.com/is/image/`是图像服务URL；`Scene7SharedAssets/ImageSet-Views-Sample`是资源：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是一个简单网页的完整示例，该网页嵌入了具有固定大小的内联缩放查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 高度不受限制的响应式设计嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

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

将查看器添加到此类页面与嵌入固定大小的步骤类似。 唯一的区别是，必须使用以相对单位设置的大小覆盖默认查看器CSS的固定大小。

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同，但以下三个例外：

* 将容器`DIV`添加到现有“持有者”`DIV`；
* 添加了具有显式断点的`imagereload`参数；
* CSS将查看器`width`和`height`设置为100%，而不是使用绝对单位设置固定的查看器大小，如下所示：

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下代码是一个完整的示例。 请注意当浏览器调整大小时查看器大小如何变化，以及查看器纵横比如何与资源匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hans)

## 定义宽度和高度的灵活大小嵌入 {#section-0a329016f9414d199039776645c693de}

如果定义了宽度和高度的灵活大小嵌入，则网页样式会不同。 它为`"holder"` DIV提供两种大小，并将其放在浏览器窗口中居中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%。

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

其余嵌入步骤与用于高度不受限制的响应式设计嵌入的步骤相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用基于Setter的API进行嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会接受任何参数，配置参数是使用`setContainerId()`、`setParam()`和`setAsset()` API方法通过单独的JavaScript调用指定的。

以下示例说明了如何将固定大小嵌入与基于setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
