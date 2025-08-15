---
title: 缩放
description: 缩放查看器是显示可缩放图像的图像查看器。 此查看器适用于图像集，并且使用样本完成导航。 它具有缩放工具、全屏支持、色板和可选的关闭按钮。 它设计为可在台式机和移动设备上工作。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 0%

---

# 缩放{#zoom}

缩放查看器是显示可缩放图像的图像查看器。 此查看器适用于图像集，并且使用样本完成导航。 它具有缩放工具、全屏支持、色板和可选的关闭按钮。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型502。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用缩放查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

缩放查看器表示一个主JavaScript文件和一组帮助程序文件(单个JavaScript包含此特定查看器使用的所有SDK组件、资源、CSS)，这些文件由查看器在运行时下载。

您可以在弹出模式下使用随IS-Viewers提供的生产就绪型HTML页面，或者在嵌入模式下使用缩放查看器，其中使用文档记录的API将其集成到目标网页中。

其配置和外观设计与其他查看器的配置和外观设计类似。 所有外观设计都是通过自定义CSS实现的。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与缩放查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

缩放查看器支持其他移动设备应用程序中常见的以下触控手势。 当查看器无法处理用户的轻扫手势时，它将事件转发给Web浏览器以执行本机页面滚动。 通过此类功能，即使查看者占据了设备屏幕区域的大部分，用户仍可导航浏览页面。

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
   <td colname="col2"> <p> 选择样本中的新缩略图。 在主视图中，它隐藏或显示用户界面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>双击 </p> </td> 
   <td colname="col2"> <p> 放大一个级别，直到达到最大放大率。 下一个双击手势会将查看器重置为初始查看状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或缩小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 在样本栏中滚动样本列表。 </p> <p> 如果图像处于重置状态，且<span class="codeph"> frametransition </span>参数设置为幻灯片，则资产将随幻灯片动画更改。 对于其他<span class="codeph">帧转换</span>模式，该笔势将执行本机页面滚动。 </p> <p> 如果放大图像，它将水平移动图像。 如果将图像移动到视图边缘并在同一方向执行滑动，则手势将执行本机页面滚动。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫 </p> </td> 
   <td colname="col2"> <p> 如果图像处于重置状态，则手势将执行本机页面滚动。 </p> <p> 放大图像时，它将垂直移动图像。 如果将图像移动到视图边缘并在同一方向执行滑动，则手势执行本机页面滚动。 </p> <p> 如果该手势在样本区域内完成，则会执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

该查看器支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入缩放查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供一个链接，选中该链接后，会在单独的浏览器窗口中打开查看器。 在其他情况下，需要直接将查看器嵌入到托管页面中。 在后一种情况下，网页可能具有静态布局，或者使用响应式设计，该设计在不同的设备上或对于不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器调整大小或设备方向更改时进行调整。

此模式最适用于移动设备。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您为弹出窗口操作模式使用现成的HTML页面。 现成的HTML页面名为`ZoomViewer.html`，它位于标准IS-Viewers部署的`html5/`子文件夹下，如下所示：

`<s7viewers_root>/html5/ZoomViewer.html`

应用自定义CSS以实现页面的自定义外观。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入式模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 此选项是拥有静态布局的网页的最佳选择。

响应式设计嵌入模式假定由于查看器容器`DIV`的大小更改，运行时需要调整查看器大小。 最常见的用例是将查看器添加到使用灵活布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页调整其容器`DIV`大小的方式。 如果网页仅设置容器`DIV`的宽度，而不限制其高度，则查看器会根据所用资源的长宽比自动选择其高度。 此逻辑可确保资产完全适合视图，而不会在两侧添加任何边距。 此用例最常见于使用响应式布局框架(如Bootstrap和Foundation)的网页。

如果网页同时设置了查看器容器`DIV`的宽度和高度，则查看器会填充该区域并遵循网页提供的大小。 例如，将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

## 固定大小嵌入 {#section-44f365e6c0dd40709467a459afa82a7f}

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 定义容器DIV。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括[!DNL ZoomViewer.js]。 [!DNL ZoomViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图，在桌面系统上，缩略图位于主视图下方。 同时，查看器允许使用`setAsset()` API在运行时交换主资源。 作为开发人员，当新资产只有一个项目时，您可以控制查看器管理底部缩略图区域的方式。 可以保持外部查看器的大小不变，并使主视图增加其高度并占据缩略图区域。 或者，您可以保持主视图大小为静态并折叠外部查看器区域，让网页内容向上移动，并使用缩略图上多余的自由屏幕区域。

   要保持外部查看器边界不变，请定义`.s7zoomviewer`顶级CSS类的大小（以绝对单位表示）。 在CSS中调整大小可直接放在HTML页面上。 或者，也可以将其放入自定义查看器CSS文件中，该文件稍后将分配给Dynamic Media Classic中的查看器预设记录，或者使用样式命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义缩放查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页面中定义静态外部查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下例中查看使用固定外部查看器的行为。 请注意，在组之间切换时，外部查看器大小不会更改：

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=zh-Hans)

   要使主视图维度为静态维度，请使用`Container` `.s7zoomviewer` CSS选择器或使用`.s7container`修饰符为内部`stagesize` SDK组件定义查看器大小（以绝对单位表示）。

   下面是一个示例，用于为内部`Container` SDK组件定义查看器大小，以便在切换资源时主视图区域不会更改其大小：

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下演示页面显示了固定主视图大小的查看器行为。 请注意，在页面集之间切换时，主视图将保持静态状态，网页内容将垂直移动。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=zh-Hans)

   您可以在Dynamic Media Classic中的查看器预设记录中设置`stagesize`修饰符。 或者，您也可以使用`params`集合中的查看器初始化代码显式传递它，或者作为API调用显式传递它，如本帮助的“命令引用”部分中所述，如下所示：

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.ZoomViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init()`方法。

   配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段保存查看器容器ID的名称，并使用查看器支持的配置参数嵌套`params` JSON对象。 在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为`asset`参数传递。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载将自动继续。

   以下是创建查看器实例、将所需的最少配置选项传递给构造函数以及调用`init()`方法的示例。 此示例假定`zoomViewer`是查看器实例，`s7viewer`是占位符DIV的名称，`http://s7d1.scene7.com/is/image/`是图像服务URL，`Scene7SharedAssets/ImageSet-Views-Sample`是资产。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是一个简单网页的完整示例，该网页以固定大小嵌入视频查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 高度不受限制的响应式设计嵌入 {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 定义宽度和高度的灵活大小嵌入 {#section-3674e6c032594441a6576b7fb1de6e64}

如果定义了宽度和高度的灵活大小嵌入，则网页样式会不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
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

## 使用基于setter的API进行嵌入 {#section-44e014925f24418b900696003855c0a9}

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会接受任何参数，配置参数是使用`setContainerId()`、`setParam()`和`setAsset()` API方法通过单独的JavaScript调用指定的。

以下示例说明了如何将固定大小嵌入与基于setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
