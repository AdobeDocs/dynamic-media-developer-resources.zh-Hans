---
title: 全景查看器
description: HTML5 Panoramic Viewer是一个显示全景图像的图像查看器。 此查看器的目的是显示球面全景，也称为等矩形图像。 它支持通过陀螺运动实现自动平移和平移。 它设计为可在台式机和移动设备上工作。 虚拟现实观看模式适用于支持移动设备的设备。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5 Panoramic Viewer是一个显示全景图像的图像查看器。 此查看器的目的是显示球面全景，也称为等矩形图像。 它支持通过陀螺运动实现自动平移和平移。 它设计为可在台式机和移动设备上工作。 虚拟现实观看模式适用于支持移动设备的设备。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。


查看器类型514。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 使用全景查看器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5全景查看器表示主JavaScript文件以及查看器在运行时下载的一组帮助程序文件。 该帮助程序文件集是单个JavaScript，其中包含此特定查看器、资源、CSS使用的所有HTML5 Viewer SDK组件。
HTML5全景查看器既可以在弹出模式下使用(使用随IS-Viewers提供的生产就绪型HTML页面)，也可以在嵌入式模式下使用（使用文档记录的API将其集成到目标网页中）。
其配置和外观设计与其他HTML5查看器的配置和外观设计类似。 所有外观设计均可通过自定义CSS获得。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与HTML5全景查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5全景查看器支持通过拖动或陀螺仪移动进行自动平移和导航。

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
   <td colname="col2"> <p>自动平移和拖动以进行导航。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>触摸设备 </p> </td> 
   <td colname="col2"> <p>默认情况下，自动平移和拖动以进行导航。 在VR渲染模式下通过陀螺仪移动导航(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

该查看器支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标，但是这项支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。
全景查看器可以通过指定vrrender修饰符在虚拟现实(VR)模式下渲染全景图像。 启用vrrender后，全景图像会显示在分屏屏幕中。 一种常见的使用案例是在安装在虚拟现实头戴式耳机中的移动电话中提供图像，为每个眼睛提供单独的图像。 观看者响应头部的陀螺仪移动并浏览图像。

## 嵌入HTML5全景查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供链接。 选择该链接将在单独的浏览器窗口中打开查看器。 在其他情况下，可能需要将查看器嵌入到托管页面中。 在后一种情况下，网页可能具有静态布局，或者是“响应式”的，并且对于不同的设备或不同的浏览器窗口大小以不同的方式显示。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它占据整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式最适用于移动设备。 该网页使用`window.open()` JavaScript调用、正确配置的HTML元素或任何其他合适的方式加载查看器。

建议您为弹出窗口操作模式使用现成的HTML页面。 它名为[!DNL PanoramicViewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

可以通过应用自定义CSS来实现可视化自定义。

以下是HTML代码示例，该代码将在新窗口中打开查看器：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入式模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 观看者通常只占用网页的一部分空间。

主要用例是面向桌面或平板电脑设备的网页，以及根据设备类型自动调整布局的响应网页。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 对于具有静态布局的网页，该方法是最佳选择。

响应式嵌入假定查看器必须在运行时调整大小以响应其容器DIV的大小更改。 最常见的用例是将查看器添加到使用灵活布局的网页。

在响应模式下，查看器的行为方式有所不同，具体取决于网页确定其容器DIV大小的方式。 如果网页仅设置容器DIV的宽度，而不限制其高度，则查看者会根据所用资产的纵横比自动选择其高度。 此方法可确保资产完全适合视图，而不会在两侧添加任何边距。 此用例最常见于使用响应式布局框架(如Bootstrap、基础等)的网页。

否则，如果网页同时设置了查看器容器DIV的宽度和高度，则查看器会填充该区域并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括[!DNL PanoramicViewer.js]。 [!DNL PanoramicViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>仅引用页面上的主查看器JavaScript `include`文件。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，请勿直接引用查看器从`Utils.js`上下文路径(所谓的统一HTML `/s7viewers`)加载的SDK5 SDK `include`库。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的辅助查看器`includes`。
>
>
>因此，将来在部署新产品版本时，在页面上直接引用查看器使用的任何二级JavaScript `include`会破坏查看器功能。

1. 定义容器DIV。

   向要显示查看器的页面添加一个空DIV元素。 DIV元素必须定义其ID，因为此ID稍后将传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。


   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 设置查看器大小

   可以通过以绝对单位为`.s7panoramicviewer`顶级CSS类声明查看器静态大小，也可以使用修饰符`stagesize`来设置查看器的静态大小。

   CSS的大小调整可直接放置在HTML页面或自定义查看器CSS文件中，该文件稍后将分配给AOD中的查看器预设记录或者使用样式命令显式传递。 有关使用CSS设置查看器样式的更多信息，请参阅自定义查看器一节。 以下是在HTML页面中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   可以使用查看器初始化代码通过params集合或作为API调用显式传递`stagesize`修饰符，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.PanoramicViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init(`)方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有containerId字段，该字段保存查看器容器ID的名称，以及包含查看器支持的配置参数的嵌套参数JSON对象。 在这种情况下，params对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为资产参数传递。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载将自动继续。

   以下示例用于创建查看器实例、将最低必要的配置选项传递给构造函数以及调用`init()`方法。 此示例假定`panoramicViewer`是查看器实例，`s7viewer`是占位符`DIV`的名称，[!DNL http://s7d1.scene7.com/is/image/]是图像服务URL，[!DNL Scene7SharedAssets/PanoramicImage-Sample]是资源。

   ```html {.line-numbers}
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

   ```html {.line-numbers}
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

**高度不受限制的响应式设计嵌入**

通过响应式嵌入，网页通常具有某种灵活的布局，可指示查看者的容器DIV的运行时大小。 在本例中，我们假设网页允许查看器的容器DIV占用Web浏览器窗口大小的80%，并且其高度不受限制。 HTML代码的网页可能如下所示：

```html {.line-numbers}
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

将查看器添加到此类页面与嵌入固定大小类似，唯一的区别是无需显式定义查看器大小：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 容器DIV应添加到现有的“所有者”DIV中。 以下代码是一个完整的示例，您可能会看到在调整浏览器大小时查看器大小如何变化，以及查看器纵横比如何与资源匹配。

```html {.line-numbers}
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

以下示例页面说明了如何更真实地使用高度不受限制的响应式设计嵌入：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=zh-Hans)

**定义了宽度和高度的响应式设计嵌入**

如果有定义了宽度和高度的响应式设计嵌入，则网页样式将不同；它为“所有者” `DIV`提供大小，并将其居中在浏览器窗口中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%：

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

其余嵌入步骤与高度不受限制的响应式嵌入相同。 产生的示例为

```html {.line-numbers}
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

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 在该API中，构造函数不接受任何参数，并且配置参数是使用具有单独的JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例说明了使用基于setter的API嵌入固定大小：

```html {.line-numbers}
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
