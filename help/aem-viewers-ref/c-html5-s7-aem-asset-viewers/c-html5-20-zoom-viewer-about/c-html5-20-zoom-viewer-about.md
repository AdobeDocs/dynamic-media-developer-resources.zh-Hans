---
description: “缩放查看器”是显示可缩放图像的图像查看器。 此查看器可处理图像集，并可使用色板完成导航。 它具有缩放工具、全屏支持、色板和可选的关闭按钮。 它设计为可在桌面和移动设备上使用。
keywords: 响应
solution: Experience Manager
title: Zoom
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2423'
ht-degree: 0%

---


# 缩放{#zoom}

“缩放查看器”是显示可缩放图像的图像查看器。 此查看器可处理图像集，并可使用色板完成导航。 它具有缩放工具、全屏支持、色板和可选的关闭按钮。 它设计为可在桌面和移动设备上使用。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型502。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## 使用缩放查看器{#section-e6c68406ecdc4de781df182bbd8088b4}

Zoom Viewer表示主JavaScript文件和一组帮助文件（单个JavaScript包含在查看器在运行时下载的由此特定查看器、资源、CSS使用的所有查看器SDK组件中）。

您可以使用随IS-Viewers提供的生产就绪型HTML页面在弹出模式中使用缩放查看器，或者在嵌入模式中使用文档化的API将缩放查看器集成到目标网页中。

配置和外观设置与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅所有查看器的通用命令参考 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看器通用的通用命令参考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[[

## 与缩放查看器{#section-642e66ca38cd4032992840ec6c0b0cd2}交互

缩放查看器支持其他移动应用程序中常见的以下触控手势。 当查看器无法处理用户的轻扫手势时，它将事件转发到Web浏览器以执行本机页面滚动。 即使查看器占据设备屏幕的大部分区域，用户也可通过这种功能在页面中导航。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手势 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>单击 </p> </td> 
   <td colname="col2"> <p> 在色板中选择新缩览图。 在主视图中，它隐藏或显示用户界面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>多次点击 </p> </td> 
   <td colname="col2"> <p> 放大一个级别，直到达到最大放大率。 下一个多次点击手势将查看器重置为初始查看状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或缩小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻击 </p> </td> 
   <td colname="col2"> <p> 滚动浏览色板条中色板的列表。 </p> <p> 如果图像处于重置状态，且<span class="codeph"> frametransition </span>参数设置为slide，则资产会随幻灯片动画一起更改。 对于其他<span class="codeph">帧转换</span>模式，手势将执行本机页面滚动。 </p> <p> 如果放大图像，则图像会水平移动图像。 如果图像移动到视图边缘，并且按相同方向执行轻扫，则手势将执行本机页面滚动。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫 </p> </td> 
   <td colname="col2"> <p> 如果图像处于重置状态，则手势将执行本机页面滚动。 </p> <p> 放大图像后，图像会垂直移动。 如果图像移动到视图边缘，并且按相同方向执行轻扫，则手势将执行本机页面滚动。 </p> <p> 如果在色板区域内完成手势，则执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

查看器支持在Windows设备上通过触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器完全可通过键盘访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入缩放查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看器行为有不同的需求。 有时网页会提供一个链接，单击该链接后，将在单独的浏览器窗口中打开查看器。 在其他情况下，需要将查看器直接嵌入到托管页面中。 在后一种情况下，网页可能具有静态布局，或者使用响应式设计，该设计在不同设备上显示不同，或针对不同的浏览器窗口大小显示不同。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式是移动设备最常见的模式。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议对弹出操作模式使用现成的HTML页。 现成的HTML页称为`ZoomViewer.html`，它位于标准IS-Viewer部署的`html5/`子文件夹下，如下所示：

`<s7viewers_root>/html5/ZoomViewer.html`

应用自定义CSS以实现页面的自定义外观。

以下是在新窗口中打开查看器的HTML代码示例：

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常仅占据网页的一部分空间。

主要用例是面向桌面或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 此选项是具有静态布局的网页的最佳选择。

响应式设计嵌入模式假定由于查看器容器`DIV`的大小变化，在运行时必须调整查看器的大小。 最常见的用例是将查看器添加到使用灵活布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页大小其容器`DIV`的方式而异。 如果网页仅设置容器的宽度`DIV`，而保持高度不受限，则查看器会根据所使用资产的宽高比自动选择其高度。 此逻辑可确保资产完美地适合视图，而不会在两侧填充任何内边。 此用例是使用响应式布局框架(如Bootstrap、Foundation等)的网页中最常见的用例。

如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器将填充该区域并遵循网页提供的大小。 例如，将查看器嵌入到模式叠加中，其中的叠加会根据Web浏览器窗口大小进行调整。

## 固定大小嵌入{#section-44f365e6c0dd40709467a459afa82a7f}

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标签。 在使用查看器API之前，请确保包含[!DNL ZoomViewer.js]。 [!DNL ZoomViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并从同一域提供，则可以使用相对路径。 否则，您将指定一个指向安装了IS-Viewer的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用由查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是，`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生变化。 Adobe不会将旧版次查看器`includes`保留在服务器上。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时破坏查看器功能。

1. 定义容器DIV。

   向希望查看器显示的页面添加空DIV元素。 DIV元素必须定义其ID，因为此ID稍后会传递到查看器API。

   占位符DIV是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小。

   此查看器在处理多项目集时显示缩略图，在桌面系统上，缩略图放在主视图下方。 同时，查看器允许使用`setAsset()` API在运行时交换主资产。 作为开发人员，您可以控制当新资产只有一个项目时，查看器如何管理底部的缩略图区域。 可以保持外部查看器的大小不变，并让主视图增加其高度并占用缩览图区域。 或者，您可以保持主视图大小为静态，并折叠外部查看器区域，让网页内容向上移动，以及使用缩略图中剩余的免费屏幕空间。

   要保持外部查看器边界不变，请以绝对单位定义`.s7zoomviewer`顶级CSS类的大小。 CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配到Dynamic Media Classic中的查看器预设记录，或使用样式命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义缩放查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页中定义静态外部查看器大小的示例：

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在下面的示例中查看具有固定外部查看器的行为。 请注意，在集之间切换时，外部查看器大小不会更改：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   要使主视图尺寸保持静态，请使用`.s7zoomviewer` `.s7container` CSS选择器或使用`stagesize`修饰符，以内部`Container` SDK组件的绝对单位定义查看器大小。

   以下示例定义内部`Container` SDK组件的查看器大小，以便在切换资产时，主视图区域不会更改其大小：

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下演示页显示了具有固定主视图大小的查看器行为。 请注意，在集之间切换时，主视图保持静态，网页内容垂直移动。

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   您可以在Dynamic Media Classic的查看器预设记录中设置`stagesize`修饰符，也可以将`params`修饰符显式传递给查看器初始化代码及集合，或作为API调用进行传递，如本帮助的“命令参考”部分中所述，如下所示：

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建`s7viewers.ZoomViewer`类的实例，将所有配置信息传递给它的构造函数，并对查看器实例调用`init()`方法。

   配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称，并嵌套了`params` JSON对象，其中包含查看器支持的配置参数。 在这种情况下，`params`对象必须至少具有作为`serverUrl`属性传递的图像服务URL和作为`asset`参数传递的初始资产。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会将构建DOM延迟到网页结束。 要获得最大兼容性，请在结束`BODY`标签之前或在正文`onload()`事件上调用`init()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可能会使用分配给它的`display:none`样式将其隐藏。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例、将最少的必要配置选项传递给构造函数并调用`init()`方法的示例。 此示例假定`zoomViewer`为查看器实例，`s7viewer`为占位符DIV的名称，`http://s7d1.scene7.com/is/image/`为图像服务URL，`Scene7SharedAssets/ImageSet-Views-Sample`为资产。

   ```
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

   以下代码是嵌入具有固定大小的视频查看器的次要网页的完整示例：

   ```
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

## 无限制高度{#section-b9ca11a7e7aa4f74ab43244cbca37ae0}的响应式设计嵌入

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

以下示例页面演示了无限制高度的响应式设计嵌入在现实生活中的更多用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

## 定义了宽度和高度{#section-3674e6c032594441a6576b7fb1de6e64}的灵活大小嵌入

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页会将`HTML`和`BODY`元素的大小设置为100%。

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

## 使用基于setter的API {#section-44e014925f24418b900696003855c0a9}进行嵌入

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会使用任何参数和配置参数，这些参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例说明如何将固定大小嵌入与基于setter的API结合使用：

```
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

