---
description: 弹出查看器是一个图像查看器。 它会显示一个静态图像，其缩放版本显示在用户激活的弹出视图中。 此查看器可处理图像集，并且导航过程可使用色板完成。 它适用于台式机和移动设备。
keywords: 响应式
solution: Experience Manager
title: 弹出
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 0%

---

# 弹出{#flyout}

弹出查看器是一个图像查看器。 它会显示一个静态图像，其缩放版本显示在用户激活的弹出视图中。 此查看器可处理图像集，并且导航过程可使用色板完成。 它适用于台式机和移动设备。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型为504。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用弹出查看器 {#section-f21ac23d3f6449ad9765588d69584772}

弹出查看器表示主JavaScript文件和一组帮助程序文件（单个JavaScript包含该查看器在运行时下载的该特定查看器、资产和CSS所使用的所有查看器SDK组件）

弹出查看器仅用于嵌入式使用，这意味着它是使用记录在案的API集成到网页中的。 弹出查看器没有可用于生产的网页。

配置和外观设置与其他查看器类似。 您可以使用自定义CSS来应用外观设置。

请参阅所有查看器的通用命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[

## 与弹出查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

弹出查看器支持其他移动设备应用程序中常见的单点触控和多点触控手势。

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
   <td colname="col2"> <p> 激活弹出视图或主缩放级别和次缩放级别之间的更改。 </p> </td> 
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

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入弹出查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或者针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持两种主要操作模式：固定大小嵌入和响应式设计嵌入。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入模式。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入模式假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在弹出查看器中使用响应式设计嵌入模式时，请确保使用`imagereload`参数为主视图图像指定明确的断点。 理想情况下，请按照网页CSS的指示，将断点与查看器宽度断点进行匹配。

在响应式设计嵌入模式下，查看器的行为方式与网页大小容器`DIV`的方式不同。 如果网页仅设置容器的宽度`DIV`，并且不限制其高度，则查看器会根据所使用资产的宽高比自动选择其高度。 这意味着资产会完美地放入视图中，侧边不会有任何内边距。 对于使用响应式设计布局框架(如Bootstrap、基础等)的网页，此特定用例最为常见。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的用例示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML标头中添加脚本标记。 在使用查看器API之前，请确保包含`FlyoutViewer.js`。 `FlyoutViewer.js` 位于标准IS查看器 [!DNL html5/js/] 部署的以下子文件夹中：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在其中一个Adobe的Dynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装IS-Viewer的AdobeDynamic Media服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能会在运行时由查看器的逻辑下载。 特别是，切勿直接引用查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生更改。 Adobe不会在服务器上保留旧版次查看器`includes`。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时中断查看器功能。

1. 定义容器DIV。

   在希望查看器显示的页面中添加空DIV元素。 必须定义DIV元素的ID，因为此ID稍后会传递到查看器API。

   占位符DIV是放置元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   网页负责为占位符DIV元素指定适当的`z-index`。 这样做可确保查看器的弹出部分显示在其他网页元素的顶部。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图。 在桌面系统上，缩略图位于主视图的下方。 同时，查看器允许在运行时使用`setAsset()` API交换主资产。 作为开发人员，当新资产只有一个项目时，您可以控制查看器如何管理底部区域的缩略图区域。 可以保持外部查看器大小不变，并让主视图增加其高度并占用缩略图区域。 或者，您也可以将主视图大小保持为静态，并折叠外部查看器区域，从而允许网页内容向上移动，然后使用缩略图中剩余的免费页面空间。

   要保持外部查看器边界不变，请以绝对单位定义`.s7flyoutviewer`顶级CSS类的大小。 CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配给Dynamic Media Classic中的查看器预设记录，或使用style命令显式传递。

   请参阅[自定义弹出查看器](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) ，以了解有关使用CSS为查看器设置样式的更多信息。

   以下是在HTML页面中定义静态外部查看器大小的示例：

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在以下示例页面上看到具有固定外部查看器区域的行为。 请注意，在集之间切换时，外部查看器大小不会发生更改：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   要使主视图维度保持静态，请使用`.s7flyoutviewer .s7container` CSS选择器为内部`Container` SDK组件定义查看器大小（以绝对单位表示）。 此外，您还应通过将默认查看器CSS中的`.s7flyoutviewer`顶级CSS类设置为`auto`来覆盖其定义的固定大小。

   以下示例用于为内部`Container` SDK组件定义查看器大小，以便在切换资产时，主视图区域不会更改其大小：

   ```
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

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   此外，请注意，默认查看器CSS为其现成外部区域提供了固定大小。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个`s7viewers.FlyoutViewer`类的实例，将所有配置信息传递给其构造函数，并在查看器实例中调用`init()`方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称，以及嵌套的`params` JSON对象，该对象具有查看器支持的配置参数。 在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为`asset`参数传递。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大的兼容性，请在结束`BODY`标记之前或在主体`onload()`事件上调用`init()`方法。

   同时，容器元素不一定只是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式来隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此情况时，查看器加载会自动恢复。

   以下示例用于创建一个查看器实例，将所需的最小配置选项传递给构造函数并调用`init()`方法。 该示例假定`flyoutViewer`为查看器实例；`s7viewer`是占位符`DIV`的名称；`http://s7d1.scene7.com/is/image/`是图像服务URL;且`Scene7SharedAssets/ImageSet-Views-Sample`为资产：

   ```
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

   以下代码是嵌入具有固定大小的弹出查看器的普通网页的完整示例：

   ```
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

## 具有无限制高度的响应式设计嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

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

将查看器添加到此类页面的步骤与固定大小嵌入的步骤类似。 唯一的区别在于，您需要使用以相对单位设置的大小，覆盖默认查看器CSS中的固定大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入相同，但有以下三个例外：

* 将容器`DIV`添加到现有的“holder” `DIV`中；
* 添加了具有明确断点的`imagereload`参数；
* 与使用绝对单位设置固定查看器大小不同，CSS会将查看器宽度和高度设置为100%，如下所示：

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

以下代码是一个完整的示例。 请注意在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```
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

以下示例页面展示了在不受限高度下响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## 定义宽度和高度的灵活大小嵌入 {#section-0a329016f9414d199039776645c693de}

在定义了宽度和高度的灵活大小嵌入时，网页样式会有所不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，该网页还会将`HTML`和`BODY`元素的大小设置为100%。

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

其余嵌入步骤与无限制高度的响应式设计嵌入步骤相同。 结果示例如下：

```
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

## 使用基于Setter的API嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会获取任何参数，并且配置参数是使用`setContainerId()`、`setParam()`和`setAsset()` API方法通过单独的JavaScript调用指定的。

以下示例说明了如何在基于setter的API中使用固定大小嵌入：

```
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
