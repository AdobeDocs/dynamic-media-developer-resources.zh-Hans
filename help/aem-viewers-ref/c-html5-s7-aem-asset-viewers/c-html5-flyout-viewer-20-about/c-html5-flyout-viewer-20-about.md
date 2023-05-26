---
title: 弹出
description: 弹出查看器是一个图像查看器。 它显示一个静态图像，该图像带有用户激活的弹出视图中所显示的缩放版本。 此查看器可处理图像集，并且使用样本完成导航。 它设计为可在台式机和移动设备上工作。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# 弹出{#flyout}

弹出查看器是一个图像查看器。 它显示一个静态图像，该图像带有用户激活的弹出视图中所显示的缩放版本。 此查看器可处理图像集，并且使用样本完成导航。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型为504。

参见 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用弹出查看器 {#section-f21ac23d3f6449ad9765588d69584772}

弹出查看器表示一个主JavaScript文件和一组帮助文件（单个JavaScript包含由此特定查看器使用的所有Viewer SDK组件、资产、CSS），这些文件由查看器在运行时下载

弹出查看器仅用于嵌入式用途，这意味着它使用文档记录的API集成到网页中。 没有可用于弹出查看器的生产就绪网页。

其配置和外观设计与其他查看器的配置和外观设计类似。 您可以使用自定义CSS来应用外观设置。

参见 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与弹出查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

弹出查看器支持在其他移动设备应用程序中常见的单点触控和多点触控手势。

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
   <td colname="col2"> <p> 激活弹出视图或在主要缩放级别和次要缩放级别之间更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 在色板栏中滚动浏览色板列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫 </p> </td> 
   <td colname="col2"> <p>如果笔势在样本区域中完成，它将执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

该查看器还支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

参见 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入弹出查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为有不同的需求。 网页可能具有静态页面布局，或者使用响应式设计，该设计在不同的设备上显示不同，或者用于不同的浏览器窗口大小。 为了满足这些需求，查看器支持两种主要操作模式：固定大小嵌入和响应式设计嵌入。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入模式。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入模式假定查看器必须在运行时调整大小以响应其容器的大小更改 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在弹出查看器中使用响应式设计嵌入模式时，请确保使用 `imagereload` 参数。 理想情况下，将断点与网页CSS指令的查看器宽度断点相匹配。

在响应式设计嵌入模式下，查看器的行为方式因网页容器的方式而异 `DIV` 大小。 如果网页仅设置容器的宽度 `DIV`，并保持其高度不受限制，则查看器会根据所用资源的纵横比自动选择其高度。 这项功能意味着资源可以完美地融入视图，而不需要两侧任何边距。 此特定用例最常见于使用响应式设计布局框架(如Bootstrap和Foundation)的网页。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的用例示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要您在HTML头中添加脚本标记。 在使用查看器API之前，请确保包括 `FlyoutViewer.js`. `FlyoutViewer.js` 如下所示 [!DNL html5/js/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在某个AdobeDynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，请指定已安装IS-Viewers的某个AdobeDynamic Media服务器的完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件。 请勿在网页代码中引用任何可能由查看器的逻辑在运行时下载的其他JavaScript文件。 特别是，请勿直接引用HTML5 SDK `Utils.js` 由查看器加载的库，从 `/s7viewers` 上下文路径（所谓的整合SDK） `include`)。 原因在于 `Utils.js` 或类似的运行时查看器库完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不保留辅助查看器的旧版本 `includes` 在服务器上。
>
>
>因此，直接引用任何辅助JavaScript `include` 将来部署新产品版本时，页面上查看器使用的功能会中断查看器。

1. 定义容器DIV。

   向要显示查看器的页面中添加一个空DIV元素。 DIV元素必须定义其ID，因为此ID稍后会被传递到查看器API。

   占位符DIV是一个定位元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   网页有责任指定 `z-index` 占位符DIV元素的位置。 这样做可确保查看器的弹出部分显示在其他网页元素的上方。

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图。 在桌面系统上，缩略图放在主视图下方。 同时，查看器允许在运行时使用交换主资源 `setAsset()` API。 作为开发人员，当新资产只有一个项目时，您可以控制查看器管理底部区域中缩略图区域的方式。 可以保持外部查看器大小不变，并让主视图增加其高度并占据缩略图区域。 或者，您可以保持主视图大小为静态并折叠外部查看器区域，让网页内容向上移动，然后使用缩略图上剩余的自由页面空间。

   要保持外部查看器边界不变，请定义 `.s7flyoutviewer` 以绝对单位表示的顶级CSS类。 CSS大小调整可以直接放在“HTML”页面或自定义查看器CSS文件中，稍后可将其分配给Dynamic Media Classic中的查看器预设记录，也可以使用style命令显式传递。

   参见 [自定义弹出查看器](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) 有关使用CSS为查看器设置样式的更多信息。

   以下是在HTML页中定义静态外部查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下面的示例页面上看到带有固定外部查看器区域的行为。 请注意，在集之间切换时，外部查看器大小不会更改：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   要使主视图尺寸为静态尺寸，请以绝对单位为内部视图定义查看器大小 `Container` 使用的SDK组件 `.s7flyoutviewer .s7container` css选择器。 此外，您应该覆盖为定义的固定大小 `.s7flyoutviewer` 默认查看器CSS中的顶级CSS类，方法是将其设置为 `auto`.

   以下是定义内部视图的查看器大小的示例 `Container` SDK组件，以便在切换资源时主视图区域不会更改其大小：

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

   以下示例页面显示了固定主视图大小的查看器行为。 请注意，在页面集之间切换时，主视图将保持静态，网页内容将垂直移动：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   此外，默认查看器CSS为其外部区域提供固定大小的现成可用大小。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.FlyoutViewer` 类，将所有配置信息传递到其构造函数，并调用 `init()` 方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有 `containerId` 保存查看器容器ID名称并嵌套的字段 `params` 包含查看器支持的配置参数的JSON对象。 在本例中， `params` 对象必须至少将图像服务URL传递为 `serverUrl` 资产，而初始资产为 `asset` 参数。 基于JSON的初始化API允许您使用一行代码创建和启动查看器。

   将查看器容器添加到DOM很重要，这样查看器代码就可以按其ID找到容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大的兼容性，请调用 `init()` 紧靠结束位置之前的方法 `BODY` 标签上，或正文上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可使用以下方式隐藏该内容： `display:none` 为其分配的样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载会自动恢复。

   以下示例介绍了如何创建查看器实例，将所需的最少配置选项传递给构造函数并调用 `init()` 方法。 此示例假定 `flyoutViewer` 是查看器实例； `s7viewer` 是占位符的名称 `DIV`； `http://s7d1.scene7.com/is/image/` 是图像服务URL；以及 `Scene7SharedAssets/ImageSet-Views-Sample` 是资产：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是嵌入固定大小弹出查看器的普通网页的完整示例：

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
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## 高度不受限制的响应式设计嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器的运行时大小 `DIV`. 对于以下示例，假设网页允许查看器的容器 `DIV` 将网页浏览器窗口大小的40%保留为无限制高度。 网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入的步骤类似。 唯一的区别是，必须使用以相对单位设置的大小覆盖默认查看器CSS的固定大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同，但有以下三个例外：

* 添加容器 `DIV` 至现有“持有人” `DIV`；
* 已添加 `imagereload` 带显式断点的参数；
* 与使用绝对单位设置固定的查看器大小不同，请使用CSS将查看器宽度和高度设置为100%，如下所示：

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下代码是一个完整的示例。 请注意浏览器调整大小时查看器大小的变化情况，以及查看器长宽比与资源的匹配情况。

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 定义宽度和高度的灵活大小嵌入 {#section-0a329016f9414d199039776645c693de}

如果定义了宽度和高度的灵活大小嵌入，则网页的样式会不同。 它将两种大小提供给 `"holder"` DIV并将其置于浏览器窗口中居中。 此外，该网页还设置 `HTML` 和 `BODY` 元素为100%。

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

其余嵌入步骤与用于高度不受限制的响应式设计嵌入的步骤相同。 产生的示例如下：

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
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用基于Setter的API进行嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不接受任何参数，并且配置参数是使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法，具有单独的JavaScript调用。

以下示例说明了如何将固定大小嵌入与基于setter的API结合使用：

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
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
