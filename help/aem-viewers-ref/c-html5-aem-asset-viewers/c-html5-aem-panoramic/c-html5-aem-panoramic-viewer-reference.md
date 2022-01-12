---
title: 全景查看器
description: HTML5全景查看器是一种显示全景图像的图像查看器。 此查看器的目的是显示球形全景图，也称为等长形图像。 它通过陀螺运动支持自动平移和平移。 它适用于台式机和移动设备。 虚拟现实查看模式在支持移动设备上可用。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5全景查看器是一种显示全景图像的图像查看器。 此查看器的目的是显示球形全景图，也称为等长形图像。 它通过陀螺运动支持自动平移和平移。 它适用于台式机和移动设备。 虚拟现实查看模式在支持移动设备上可用。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


查看器类型514。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 使用全景查看器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5全景查看器表示主JavaScript文件以及查看器在运行时下载的一组帮助程序文件。 帮助程序文件集是一个JavaScript包含文件，其中包含此特定查看器、资产和CSS使用的所有HTML5查看器SDK组件。
HTML5全景查看器既可以在弹出模式下使用IS-Viewer提供的生产就绪HTML页，也可以在嵌入式模式下使用，在嵌入式模式下，可以使用记录在案的API将其集成到目标网页中。
配置和外观设置与其他HTML5查看器的配置和外观设置类似。 所有外观设置都可以通过自定义CSS实现。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器 — URL通用的命令引用](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与HTML5全景查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5全景查看器通过拖动或回转运动支持自动平移和导航。

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>导航 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>桌面 </p> </td> 
   <td colname="col2"> <p>自动平移并拖动以进行导航。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>触控设备 </p> </td> 
   <td colname="col2"> <p>默认情况下，自动平移和拖动以进行导航。 在VR渲染模式下通过陀螺仪移动进行导航(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

在Windows设备上，查看器通过触摸屏和鼠标同时支持触摸输入和鼠标输入，但此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。
全景查看器可以通过指定vrrender修饰符，在虚拟现实(VR)模式下渲染全景图像。 启用vrrender后，全景图像会显示在拆分屏幕中。 一个常见用例是在安装在虚拟现实头戴式耳机中的移动电话中提供图像，为每只眼睛提供单独的图像。 观看者响应头的陀螺运动并浏览图像。

## 嵌入HTML5全景查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时网页会提供链接。 选择该链接会在单独的浏览器窗口中打开查看器。 在其他情况下，可能需要将查看器嵌入到托管页面中。 在后一种情况下，网页可能具有静态布局，或者是“响应式”，并且在不同设备上或针对不同浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式嵌入。

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向发生更改时进行调整。

此模式是移动设备最常使用的模式。 网页使用 `window.open()` JavaScript调用、正确配置的HTML元素或任何其他合适的方式。

建议您使用现成的HTML页面进行弹出操作模式。 它名为 [!DNL PanoramicViewer.html] 它位于 [!DNL html5/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

可通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占网页的一部分房地产。

主要用例包括面向台式机或平板电脑设备的网页，以及响应式网页，这些网页可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 此方法是具有静态布局的网页的最佳选择。

响应式嵌入假定查看器必须在运行时调整大小以响应其容器DIV的大小更改。 最常见的用例是将查看器添加到使用灵活布局的网页。

在响应模式下，查看器的行为方式会因网页大小其容器DIV的方式而异。 如果网页仅设置容器DIV的宽度，且高度不受限制，则查看器会根据所用资产的宽高比自动选择其高度。 此方法可确保资产完美地适合视图，而不会在侧边添加任何内边距。 对于使用响应式布局框架(如Bootstrap、基础等)的网页，此用例最为常见。

否则，如果网页同时设置查看器容器DIV的宽度和高度，则查看器将填充该区域并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中的叠加将根据Web浏览器窗口大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML头中添加脚本标记。 在使用查看器API之前，请确保在 [!DNL PanoramicViewer.js]. 的 [!DNL PanoramicViewer.js] 文件位于 [!DNL html5/js/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果查看器部署在其中一个Adobe Dynamic Media Classic服务器上并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装IS-Viewers的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件。 请勿在网页代码中引用任何可能由查看器逻辑在运行时下载的其他JavaScript文件。 特别是，请勿直接引用HTML5 SDK `Utils.js` 查看器从 `/s7viewers` 上下文路径(所谓的整合SDK `include`)。 原因是 `Utils.js` 或者，查看器的逻辑以及查看器版本之间的位置更改将完全管理类似的运行时查看器库。 Adobe不会保留旧版次查看器 `includes` 在服务器上。
>
>
>因此，应直接引用任何辅助JavaScript `include` 当部署了新产品版本时，查看器在页面上的使用会在未来中断查看器功能。

1. 定义容器DIV。

   在希望查看器显示的页面中添加空DIV元素。 必须定义DIV元素的ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是放置元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.


   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 设置查看器大小

   您可以通过声明查看器的静态大小 `.s7panoramicviewer` 以绝对单位表示的顶级CSS类，或使用修饰符 `stagesize`.

   CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配给AOD中的查看器预设记录，或者使用style命令显式传递。 有关使用CSS为查看器设置样式的更多信息，请参阅自定义查看器一节。 以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 修饰符可以通过参数集合的查看器初始化代码显式传递，或作为API调用（如命令引用部分中所述）传递，如下所示：

   ```
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   建议使用基于CSS的方法，该方法将在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.PanoramicViewer` 类，将所有配置信息传递给其构造函数并调用 `init(`)方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有containerId字段，该字段包含查看器容器ID的名称以及嵌套参数JSON对象（具有查看器支持的配置参数）。 在这种情况下，参数对象必须至少将图像服务URL作为 `serverUrl` 资产和初始资产。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大兼容，请调用 `init()` 方法 `BODY` 标记，或在主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用 `display:none` 样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此操作时，查看器加载会自动恢复。

   以下示例用于创建查看器实例、向构造函数传递最小必需配置选项以及调用 `init()` 方法。 此示例假定 `panoramicViewer` 是查看器实例， `s7viewer` 是占位符的名称 `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 是图像提供URL， [!DNL Scene7SharedAssets/PanoramicImage-Sample] 是资产。

   ```
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   以下代码是嵌入具有固定大小的全景查看器的普通网页的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**具有无限制高度的响应式设计嵌入**

通过响应式嵌入，网页通常具有某种灵活的布局，这指示了查看器容器DIV的运行时大小。 就本例而言，假设网页允许查看者的容器DIV占用Web浏览器窗口大小的80%，并且其高度不受限制。 网页HTML代码可能如下所示：

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

将查看器添加到此类页面与固定大小嵌入类似，只有区别在于，您无需明确定义查看器大小：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同。 应将容器DIV添加到现有“保持器”DIV中。 以下代码是一个完整的示例，您可能会看到在调整浏览器大小时查看器大小的变化情况，以及查看器宽高比与资产的匹配情况。

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

以下示例页面展示了如何在现实中使用高度不受限制的响应式设计嵌入：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

[替代演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定义宽度和高度的响应式设计嵌入**

如果定义了响应式设计嵌入的宽度和高度，则网页的样式会有所不同；它为“holder”提供两种大小 `DIV` 并在浏览器窗口中居中显示。 此外，网页还会设置 `HTML` 和 `BODY` 元素到100%:

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

其余的嵌入步骤与具有不受限高度的响应式嵌入相同。 结果示例为

```
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**使用基于Setter的API嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API时，构造函数不会获取任何参数，并且配置参数是使用 `setContainerId()`, `setParam()`和 `setAsset()` 包含单独JavaScript调用的API方法。

以下示例说明了使用基于setter的API进行固定大小嵌入的方法：

```
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
