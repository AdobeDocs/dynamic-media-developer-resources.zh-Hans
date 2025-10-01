---
title: 轮盘式
description: 轮播查看器是一个查看器，可显示带有可单击热点或区域的不可缩放横幅图像的轮播。 此查看器可以帮助您实施“可购物轮播”体验，以便用户可以在横幅图像上选择热点或区域。 他们可能会被重定向到客户网站上的概览或产品详细信息页面。 它设计为可在台式机和移动设备上工作。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1851'
ht-degree: 0%

---

# 轮盘式{#carousel}

轮播查看器是一个查看器，可显示带有可单击热点或区域的不可缩放横幅图像的轮播。 此查看器可以帮助您实施“可购物轮播”体验，以便用户可以在横幅图像上选择热点或区域。 他们可能会被重定向到客户网站上的概览或产品详细信息页面。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用图像渲染或用户生成内容(UGC)的图像。

查看器类型为511。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--
[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html?lang=zh-Hans)
-->

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅[系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用轮播查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

轮播查看器表示一个主JavaScript文件和一组帮助程序文件(单个JavaScript包含此特定查看器使用的所有SDK组件、资源、CSS)，这些文件由查看器在运行时下载。

轮播查看器既可以在弹出模式下使用(随IS查看器提供，可用于生产就绪的HTML页面)，也可以在嵌入式模式下使用（使用文档记录的API将其集成到目标网页中）。

配置和外观设计类似于本帮助中描述的其他查看器的配置和外观。 所有外观设计都是通过自定义CSS实现的。

查看所有查看者通用的[命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与轮播查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

使用在主视图上水平轻扫或桌面设备上提供的两个箭头按钮，可以浏览轮播集。 设置指示符点显示设置内当前的位置。

查看器可以在横幅图像上方渲染热点或区域，以指示产品上的交互区域。

在创作期间，单击或点按热点或区域会触发与其关联的操作。 该动作可以被重定向到网站上的不同页面，或者它可以将产品信息传递回网页逻辑，该网页逻辑又可以触发带有相关产品内容的快速查看。

查看器完全可使用键盘。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入轮播查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器调整大小或移动设备的方向更改时进行调整。

弹出模式是移动设备中最常见的一种模式。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您为弹出窗口操作模式使用现成的HTML页面。 在这种情况下，该文件夹名为`CarouselViewer.html`，位于标准IS-Viewers部署的`html5/`子文件夹中：

`<s7viewers_root>/html5/CarouselViewer.html`

您可以通过应用自定义CSS来实现可视化自定义。

<!--
The following is an example of HTML code that opens the viewer in a new window:

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```
-->

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入式模式下，查看器将添加到现有网页中。 此网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例包括面向台式机或平板电脑设备的网页，以及可根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 对于具有静态布局的网页，此方法为最佳选择。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器`DIV`的大小更改。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页调整其容器`DIV`大小的方式。 如果网页仅设置容器`DIV`的宽度，而不限制其高度，则查看器会根据所用资源的长宽比自动选择其高度。 此功能可确保资产完全适合视图，不会出现任何边距。 此用例最常用于使用响应式Web设计布局框架(如Bootstrap和Foundation)的网页。

否则，如果网页同时设置了查看器容器`DIV`的宽度和高度，则查看器仅填充该区域。 它还遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 正在将查看器JavaScript文件添加到您的网页。

   创建查看器需要您在HTML head中添加脚本标记。 在使用查看器API之前，请确保包括[!DNL CarouselViewer.js]。 [!DNL CarouselViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>仅引用页面上的主查看器JavaScript `include`文件。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，请勿直接引用查看器从`Utils.js`上下文路径(所谓的统一HTML `/s7viewers`)加载的SDK5 SDK `include`库。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的辅助查看器`includes`。
>
>
>因此，将来在部署新产品版本时，在页面上直接引用查看器使用的任何二级JavaScript `include`会破坏查看器功能。

1. 正在定义容器`DIV`。

   向您希望查看器显示的页面添加一个空`DIV`元素。 `DIV`元素必须定义其ID，因为此ID稍后将传递到查看器API。 DIV的大小通过CSS指定。

   占位符`DIV`是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   以下是定义的占位符`DIV`元素的示例：

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   您可以通过声明查看器为`.s7carouselviewer`顶级CSS类（以绝对单位表示）或使用`stagesize`修饰符来设置查看器的静态大小。

   您可以在HTML页面上直接放置在CSS中的大小。 或者，您也可以将大小调整放入自定义查看器CSS文件中，该文件随后将根据需要分配给AEM Assets中的查看器预设记录，或者使用`style`命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义轮播查看器](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以使用查看器初始化代码通过`stagesize`集合明确传递`params`修饰符，或者作为API调用进行传递，如命令引用部分中所述，如下所示：

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，创建`s7viewers.CarouselViewer`类的实例，将所有配置信息传递到其构造函数，并在查看器实例上调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段保存查看器容器ID的名称，并嵌套`params` JSON对象，其中包含查看器支持的配置参数。 在这种情况下，`params`对象必须至少将图像服务URL作为`serverUrl`属性传递，并将初始资产作为`asset`参数传递。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大兼容性，请在结束`init()`标记之前或主体`BODY`事件上调用`onload()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 当此功能生效时，查看器加载会自动恢复。


   以下示例用于创建查看器实例、将最低必要的配置选项传递给构造函数以及调用`init()`方法。 该示例假设`carouselViewer`是查看器实例；`s7viewer`是占位符`DIV`的名称；`https://adobedemo62-h.assetsadobe.com/is/image`是图像服务URL，`/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner`是资源：

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```


   以下代码是嵌入固定大小轮盘查看器的简单网页的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器`DIV`的运行时大小。

对于以下示例，假设网页允许查看者的容器`DIV`占用Web浏览器窗口大小的40%。 而且，它的高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与嵌入固定大小的步骤类似。 唯一的区别是，您不需要显式定义查看器大小。

1. 正在将查看器JavaScript文件添加到您的网页。
1. 正在定义容器`DIV`。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 将容器`DIV`添加到现有`"holder"` `DIV`。 以下代码是一个完整的示例。 请注意当浏览器调整大小时查看器大小如何变化，以及查看器纵横比如何与资源匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用途：

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=zh-Hans](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html?lang=zh-Hans)

定义宽度和高度的&#x200B;**灵活大小嵌入**

在定义了宽度和高度的灵活大小嵌入中，网页的样式不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页将`HTML`和`BODY`元素的大小设置为100%。


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

其余嵌入步骤与用于高度不受限制的响应式嵌入的步骤相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```


**使用基于Setter的API嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会接受任何参数，配置参数是使用`setContainerId()`、`setParam()`和`setAsset()` API方法通过单独的JavaScript调用指定的。


以下示例说明了如何将固定大小嵌入与基于setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

