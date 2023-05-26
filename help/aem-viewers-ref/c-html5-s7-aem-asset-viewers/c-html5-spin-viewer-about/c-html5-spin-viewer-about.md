---
title: Spin
description: 旋转查看器是一种图像查看器，可提供图像的360度视图，甚至多维视图（如果使用适当的旋转集）。 它具有缩放和旋转工具、全屏支持和可选的关闭按钮。 它设计为可在台式机和移动设备上工作。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Spin{#spin}

旋转查看器是一种图像查看器，可提供图像的360度视图，甚至多维视图（如果使用适当的旋转集）。 它具有缩放和旋转工具、全屏支持和可选的关闭按钮。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型503。

参见 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## 使用旋转查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

旋转查看器表示一个主JavaScript文件和一组帮助文件（单个JavaScript包含此特定查看器使用的所有Viewer SDK组件、资产、CSS），这些文件由查看器在运行时下载。

旋转查看器既可以在弹出模式下使用(使用IS-Viewers提供的生产就绪HTML页)，也可以在嵌入模式下使用（使用文档记录的API将其集成到目标网页中）。

其配置和外观设计与其他查看器的配置和外观设计类似。 所有外观设计均可通过自定义CSS获得。

参见 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与旋转查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

旋转查看器支持其他移动设备应用程序中常见的以下触控手势。 当查看器无法处理用户的轻扫手势时，它将事件转发给Web浏览器以执行本机页面滚动。 此功能允许用户在页面中导航，即使查看器占据设备屏幕区域的大部分区域也是如此。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手势 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>双击 </p> </td> 
   <td colname="col2"> <p> 放大一个级别，直到达到最大放大率。 下一个双击手势会将查看器重置为初始查看状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或缩小图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 如果图像处于重置状态，它将水平旋转该集。 </p> <p> 如果放大图像，它将水平移动图像。 如果将图像移动到视图边缘，并且仍在该方向执行滑动，则该手势会执行本机页面滚动。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫或轻触 </p> </td> 
   <td colname="col2"> <p> 如果图像处于复位状态，则当使用多维旋转集时，它改变垂直视角。 在一维旋转集中，该手势执行本机页面滚动。 或者，当多维旋转集位于最后一个轴或第一个轴上以使垂直滑动不会导致垂直视角改变时，该手势还执行本机页面滚动。 </p> <p> 如果放大图像，则会垂直移动图像。 如果将图像移动到视图边缘，并且仍在该方向执行滑动，则该手势会执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>该查看器还支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

参见 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入旋转查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为有不同的需求。 有时，网页会提供一个链接，在选中该链接后，会在单独的浏览器窗口中打开查看器。 在其他情况下，需要直接将查看器嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同的设备上或对于不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会取用整个浏览器窗口区域，并在浏览器调整大小或移动设备的方向发生更改时进行调整。

弹出窗口模式最适用于移动设备。 网页使用以下方式加载查看器 `window.open()` JavaScript调用，正确配置 `A` HTML元素或任何其他合适的方法。

建议您将现成的HTML页用于弹出窗口操作模式。 在这种情况下，将调用 [!DNL SpinViewer.html] 且位于 [!DNL html5/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/html5/SpinViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入式模式下，查看器将添加到现有网页，该网页可能已有某些与查看器无关的客户内容。 查看者通常只占用网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 此操作是拥有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器的大小更改 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页确定其容器大小的方式 `DIV`. 如果网页仅设置容器的宽度 `DIV`如果不限制高度，查看器会根据所用资源的纵横比自动选择高度。 此功能可确保资源完全适合视图，而不用填充边距。 此用例最常用于使用响应式设计布局框架(如Bootstrap或Foundation)的网页。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例可能就是将查看器嵌入到模态叠加图，其中叠加图根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作可将“旋转查看器”添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要您在HTML头中添加脚本标记。 在使用查看器API之前，请确保包括 `SpinViewer.js`. `SpinViewer.js` 位于 [!DNL html5/js/] 标准IS-Viewers部署的子文件夹：

   `<s7viewers_root>/html5/js/SpinViewer.js`

   如果查看器部署在某个AdobeDynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，请指定已安装IS-Viewers的某个AdobeDynamic Media服务器的完整路径。

   相对路径如下所示：

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
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

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   通过声明查看器的静态大小，可以将其设置为 `.s7spinviewer` 以绝对单位表示的顶级CSS类，或者使用 `stagesize` 修饰符。

   您可以将CSS的大小直接放在“HTML”页面上，或放在自定义查看器CSS文件中。 之后，会将该预设分配给Dynamic Media Classic中的查看器预设记录，或者使用样式命令显式传递该预设记录。

   参见 [自定义旋转查看器](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) 有关使用CSS为查看器设置样式的更多信息。

   以下是在“HTML”页中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以设置 `stagesize` 在Dynamic Media Classic的查看器预设记录中修改该参数。 或者，您可以使用查看器初始化代码显式传递它 `params` 收藏集或API调用（如命令引用部分中所述），如下所示：

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   建议使用基于CSS的方法，并用于此示例。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.SpinViewer` 类，将所有配置信息传递到其构造函数，并调用 `init()` 方法。 配置信息作为JSON对象传递给构造函数。 此对象至少具有 `containerId` 保存查看器容器ID名称并嵌套的字段 `params` 包含查看器支持的配置参数的JSON对象。 在本例中 `params` 对象，必须至少将图像服务URL传递为 `serverUrl` 及初始资产 `asset` 参数。 基于JSON的初始化API允许您使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大的兼容性，请调用 `init()` 紧靠结束位置之前的方法 `BODY` 标签上，或正文上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用隐藏的 `display:none` 为其分配的样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载会自动恢复。

   以下示例介绍了如何创建查看器实例，将所需的最少配置选项传递给构造函数并调用 `init()` 方法。 此示例假定 `spinViewer` 是查看器实例， `s7viewer` 是占位符的名称 `DIV`， [!DNL http://s7d1.scene7.com/is/image/] 是图像服务URL，并且 [!DNL Scene7SharedAssets/SpinSet_Sample] 是资产。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是嵌入固定大小旋转查看器的普通网页的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器的运行时大小 `DIV`. 在本例中，假设网页允许查看者的容器 `DIV` 将网页浏览器窗口大小的40%保留为无限制高度。 生成的网页HTML代码如下所示：

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

将查看器添加到此类页面与嵌入固定大小类似，唯一的区别是无需明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述步骤与固定大小的嵌入步骤相同。 添加容器 `DIV` 到现有“持有人” `DIV`. 以下代码是一个完整的示例。 您可以查看浏览器调整大小时查看器大小的变化情况以及查看器长宽比与资源的匹配情况。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用例：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定义宽度和高度的灵活大小嵌入**

如果定义了宽度和高度的灵活大小嵌入，则网页的样式会不同。 即，它为“托架”提供两种尺寸 `DIV` 并将其居中在浏览器窗口中。 此外，该网页还设置 `HTML` 和 `BODY` 元素至100%：

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

其余嵌入步骤与高度不受限制的响应式设计嵌入相同。 产生的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API构造函数不接受任何参数，并且配置参数是使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法具有单独的JavaScript调用。

以下示例显示使用基于setter的API嵌入固定大小的内容：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
