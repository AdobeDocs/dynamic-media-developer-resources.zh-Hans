---
title: 内联缩放
description: 内联缩放查看器是一个图像查看器。 当用户滚动或触摸主视图时，它会显示一个静态图像，该静态图像上会显示缩放的版本。 此查看器可处理图像集，并且导航过程可使用色板完成。 它适用于台式机和移动设备。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 0%

---

# 内联缩放{#inline-zoom}

内联缩放查看器是一个图像查看器。 当用户滚动或触摸主视图时，它会显示一个静态图像，该静态图像上会显示缩放的版本。 此查看器可处理图像集，并且导航过程可使用色板完成。 它适用于台式机和移动设备。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型为504。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## 使用内联缩放查看器 {#section-f21ac23d3f6449ad9765588d69584772}

内联缩放查看器表示主JavaScript文件和一组帮助程序文件（单个JavaScript包含该查看器在运行时下载的特定查看器、资产和CSS所使用的所有查看器SDK组件）。

内联缩放查看器既可以在弹出模式下使用生产就绪型HTML页面（随图像服务查看器提供），也可以在嵌入式模式下使用，在这种模式下，可使用记录在案的API将其集成到目标网页中。

配置和外观设置与其他查看器类似。 您可以使用自定义CSS来应用外观设置。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器 — URL通用的命令引用](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与内联缩放查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

内联缩放查看器支持其他移动设备应用程序中常见的单点触控和多点触控手势。

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
   <td colname="col2"> <p> 激活弹出视图或在色板中的主缩放级别和辅助缩放级别之间进行更改，然后选择新的缩略图。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 滚动样本栏中的样本列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫 </p> </td> 
   <td colname="col2"> <p>如果手势是在色板区域内完成的，则会执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

查看器还支持在具有触摸屏和鼠标的Windows设备上输入触摸输入和鼠标。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可完全通过键盘访问。

请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入内联缩放查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时，网页会提供可单击的链接，以在单独的浏览器窗口中打开查看器。 在其他情况下，可能需要直接将查看器嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或者针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式嵌入。

**弹出窗口**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器窗口大小或设备方向发生更改时进行调整。

此模式是移动设备最常使用的模式。 网页使用 `window.open()` JavaScript调用，已正确配置 `A` HTML元素，或任何其他合适的方式。

建议您将现成的HTML页面用于名为 `FlyoutViewer.html`. 它位于 [!DNL html5/] 标准图像服务查看器部署的子文件夹：

`<s7viewers_root>/html5/FlyoutViewer.html`

还必须配置FlyoutZoomView组件以在内联缩放模式下工作。 建议您使用现成的 `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` 内联缩放查看器的预设，或从中派生的自定义预设。 可通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**固定大小嵌入和响应式嵌入**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占网页的一部分房地产。

主要用例包括面向台式机或平板电脑设备的网页，以及响应式网页，这些网页可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入模式。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入模式假定查看器必须在运行时调整大小以响应其容器的大小变化 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在内联缩放查看器中使用响应式设计嵌入模式时，请确保使用为主视图图像指定明确的断点 `imagereload` 参数。 理想情况下，请按照网页CSS的指示，将断点与查看器宽度断点进行匹配。

在响应式设计嵌入模式下，查看器的行为方式与网页容器的方式有所不同 `DIV` 大小。 如果网页仅设置容器的宽度 `DIV`，则查看器会保持高度不受限制，然后根据所使用资产的宽高比自动选择高度。 此功能意味着资产可以完美地放入视图中，且两侧没有任何边距。 对于使用响应式设计布局框架(如Bootstrap或Foundation)的网页，此特定用例最为常见。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的用例示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML头中添加脚本标记。 在使用查看器API之前，请确保在 `FlyoutViewer.js`. `FlyoutViewer.js` 在以下 [!DNL html5/js/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在其中一个Adobe的Dynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装IS-Viewer的AdobeDynamic Media服务器的完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件。 请勿在网页代码中引用任何可能由查看器逻辑在运行时下载的其他JavaScript文件。 特别是，请勿直接引用HTML5 SDK `Utils.js` 查看器从 `/s7viewers` 上下文路径(所谓的整合SDK `include`)。 原因是 `Utils.js` 或者，查看器的逻辑以及查看器版本之间的位置更改将完全管理类似的运行时查看器库。 Adobe不会保留旧版次查看器 `includes` 在服务器上。
>
>
>因此，应直接引用任何辅助JavaScript `include` 当部署了新产品版本时，查看器在页面上的使用会在未来中断查看器功能。

1. 定义容器DIV。

   在希望查看器显示的页面中添加空DIV元素。 必须定义DIV元素的ID，因为此ID稍后会传递到查看器API。

   占位符DIV是放置元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   网页负责指定 `z-index` （表示占位符DIV元素）。 这样做可确保查看器的弹出部分显示在其他网页元素的顶部。

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图。 在桌面系统上，缩略图位于主视图的下方。 同时，查看器允许在运行时使用 `setAsset()` API。 作为开发人员，当新资产只有一个项目时，您可以控制查看器如何管理底部区域的缩略图区域。 可以保持外部查看器大小不变，并让主视图增加其高度并占用缩略图区域。 或者，您也可以将主视图大小保持为静态，并折叠外部查看器区域，使网页内容向上移动，然后使用缩略图中剩余的免费页面空间。

   要保持外部查看器范围不变，请定义 `.s7flyoutviewer` 以绝对单位表示的顶级CSS类。 CSS中的大小调整可以直接放在HTML页面上，或放在自定义查看器CSS文件中，稍后在Dynamic Media Classic中分配给查看器预设记录，或使用style命令显式传递。

   请参阅 [自定义内联缩放查看器](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 有关使用CSS为查看器设置样式的更多信息。

   以下示例用于在HTML页中定义静态外部查看器大小：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在以下示例页面上看到具有固定外部查看器区域的行为。 请注意，在集之间切换时，外部查看器大小不会发生更改：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   要使主视图尺寸保持静态，请为内部定义以绝对单位表示的查看器大小 `Container` SDK组件使用 `.s7flyoutviewer .s7container` CSS选择器。 此外，您还应覆盖为 `.s7flyoutviewer` 默认查看器CSS中的顶级CSS类，方法是将其设置为 `auto`.

   以下是定义内部查看器大小的示例 `Container` SDK组件，以便在切换资产时，主视图区域不会更改其大小：

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

   以下示例页面显示主视图大小固定的查看器行为。 请注意，在集之间切换时，主视图保持静态，并且网页内容会垂直移动：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   此外，默认查看器CSS为其现成外部区域提供了固定大小。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.FlyoutViewer` 类，将所有配置信息传递给其构造函数并调用 `init()` 方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有 `containerId` 包含查看器容器ID和嵌套名称的字段 `params` 具有查看器支持的配置参数的JSON对象。 在本例中， `params` 对象必须至少将图像服务URL作为 `serverUrl` 财产；初始资产作为 `asset` 参数，将CSS加载为 `contentUrl` 参数和预设名称 `config` 参数。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大兼容，请调用 `init()` 方法 `BODY` 标记，或在主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用 `display:none` 样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此操作时，查看器加载会自动恢复。

   以下示例用于创建查看器实例，将最小必需的配置选项传递给构造函数并调用 `init()` 方法。 该示例假定 `inlineZoomViewer` 为查看器实例； `s7viewer` 是占位符的名称 `DIV`; `http://s7d1.scene7.com/is/image/` 是图像提供URL;和 `Scene7SharedAssets/ImageSet-Views-Sample` 是资产：

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

   以下代码是嵌入具有固定大小的内联缩放查看器的简单网页的完整示例：

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

## 具有无限制高度的响应式设计嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指示查看器容器的运行时大小 `DIV`. 在以下示例中，假定网页允许查看者的容器 `DIV` 可获取Web浏览器窗口大小的40%，从而使其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面的步骤与固定大小嵌入的步骤类似。 唯一的区别在于，您必须在大小以相对单位设置时，覆盖默认查看器CSS的固定大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入相同，但有以下三个例外：

* 添加容器 `DIV` 至现有“持有人” `DIV`;
* 添加 `imagereload` 具有明确断点的参数；
* 使用绝对单位设置固定查看器大小时，不要使用设置查看器的CSS `width` 和 `height` 为100%，如下所示：

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下代码是一个完整的示例。 请注意在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

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

以下示例页面展示了在不受限制高度下响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 定义宽度和高度的灵活大小嵌入 {#section-0a329016f9414d199039776645c693de}

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 它为 `"holder"` DIV并将其居中在浏览器窗口中。 此外，网页还会设置 `HTML` 和 `BODY` 元素到100%。

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

其余嵌入步骤与无限制高度的响应式设计嵌入步骤相同。 结果示例如下：

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

## 使用基于Setter的API嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会获取任何参数，并且配置参数是使用 `setContainerId()`, `setParam()`和 `setAsset()` API方法（包含单独的JavaScript调用）。

以下示例说明了如何在基于setter的API中使用固定大小嵌入：

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
