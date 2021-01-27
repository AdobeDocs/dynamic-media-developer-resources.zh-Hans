---
description: 旋转式查看器是一种查看器，它显示带有可单击热点或区域的不可缩放横幅图像的旋转式。 此查看器的目的是实现“购物轮盘”体验，用户可在横幅图像上选择热点或区域，并将其重定向到客户网站上的概览或产品详细信息页面。 它设计为可在桌面和移动设备上使用。
seo-description: 旋转式查看器是一种查看器，它显示带有可单击热点或区域的不可缩放横幅图像的旋转式。 此查看器的目的是实现“购物轮盘”体验，用户可在横幅图像上选择热点或区域，并将其重定向到客户网站上的概览或产品详细信息页面。 它设计为可在桌面和移动设备上使用。
seo-title: 轮盘式
solution: Experience Manager
title: 轮盘式
topic: Dynamic Media
uuid: 0ba4f40b-8dde-4479-b906-3115f09ab249
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1978'
ht-degree: 0%

---


# 轮盘式{#carousel}

旋转式查看器是一种查看器，它显示带有可单击热点或区域的不可缩放横幅图像的旋转式。 此查看器的目的是实现“购物轮盘”体验，用户可在横幅图像上选择热点或区域，并将其重定向到客户网站上的概览或产品详细信息页面。 它设计为可在桌面和移动设备上使用。

>[!NOTE]
>
>此查看器不支持使用图像渲染或用户生成内容(UGC)的图像。

查看器类型为511。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅[系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 使用传送查看器{#section-e6c68406ecdc4de781df182bbd8088b4}

传送查看器表示主JavaScript文件和一组帮助文件（单个JavaScript包含该查看器在运行时下载的所有查看器SDK组件、资源、CSS）。

旋转式查看器既可以在弹出模式下使用IS查看器附带的生产就绪型HTML页面，也可以在嵌入式模式下使用，在该模式下，使用文档化的API将其集成到目标网页中。

配置和外观与本帮助中描述的其他查看器的配置和外观相似。 所有外观设置都通过自定义CSS实现。

请参阅所有查看器通用的[命令引用——配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看器通用的[命令引用- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与传送查看器{#section-642e66ca38cd4032992840ec6c0b0cd2}交互

通过主视图上的水平轻扫或桌面设备上提供的两个箭头按钮，可在旋转集中导航。 设置指示符点显示设置内的当前位置。

查看器可以在横幅图像顶部渲染热点或区域，以指示产品上的交互区域。

在创作期间，单击或点按热点或区域会触发与其关联的操作。 该操作可被重定向到网站上的其他页面，或者它可以将产品信息传递回网页逻辑，而网页逻辑又可以触发包含相关产品内容的概览。

查看器完全可通过键盘访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入传送查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或移动设备的方向更改时进行调整。

弹出模式是移动设备中最常见的模式。 网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 在这种情况下，它称为`CarouselViewer.html`，位于标准IS-Viewer部署的`html5/`子文件夹中：

`<s7viewers_root>/html5/CarouselViewer.html`

通过应用自定义CSS，可以实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页。 此网页可能已包含一些与查看器无关的客户内容。 查看器通常只占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，将使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式因网页大小其容器`DIV`的方式而异。 如果网页仅设置容器`DIV`的宽度，而保持高度不受限，则查看器会根据所使用资产的长宽比自动选择其高度。 此功能可确保资产完美地适合视图，而不会在两侧添加任何边距。 此用例是使用响应式Web设计布局框架(如Bootstrap、基础等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域。 它还遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模态叠加中，其中叠加根据Web浏览器窗口大小进行大小调整。

**固定大小嵌入**

通过执行以下操作，可将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含[!DNL CarouselViewer.js]。 [!DNL CarouselViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

如果查看器部署在某个AdobeDynamic Media经典服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定到安装了IS-Viewer的AdobeDynamic Media经典服务器之一的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 在网页代码中不应引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因在于，`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不会将旧版本的辅助查看器`includes`保留在服务器上。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时中断查看器功能。

1. 定义容器`DIV`。

   将空`DIV`元素添加到希望查看器显示的页面。 `DIV`元素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符`DIV`是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   以下是定义的占位符`DIV`元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   您可以通过以下方式设置查看器的静态大小：以绝对单位声明查看器为`.s7carouselviewer`顶级CSS类，或使用`stagesize`修饰符。

   您可以将大小调整直接放在HTML页面或自定义查看器CSS文件中，该文件稍后将指定给AEM Assets的查看器预设记录——按需，或使用`style`命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义传送查看器](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以将`stagesize`修饰符与查看器初始化代码与`params`集合显式传递，或作为“命令参考”部分中所述的API调用进行传递，如下所示：

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建`s7viewers.CarouselViewer`类的实例，将所有配置信息传递给它的构造函数，并调用查看器实例的`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称和嵌套的`params` JSON对象（查看器支持配置参数）。 在这种情况下，`params`对象至少必须具有作为`serverUrl`属性传递的图像服务URL和作为`asset`参数传递的初始资产。 基于JSON的初始化API允许您使用一行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码能够按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为获得最大兼容性，请在结束`BODY`标记之前或在正文`onload()`事件中调用`init()`方法。

   同时，容器元素不一定是网页布局的一部分。 例如，它可能会使用分配给它的`display:none`样式进行隐藏。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例的示例，向构造函数传递最少的必要配置选项并调用`init()`方法。 该示例假定`carouselViewer`为查看器实例；`s7viewer`是占位符`DIV`的名称；`https://adobedemo62-h.assetsadobe.com/is/image`是图像服务URL,`/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner`是资产：

   ```
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

   以下代码是嵌入具有固定大小的传送查看器的次要网页的完整示例：

   ```
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

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，它指示查看器容器`DIV`的运行时大小。 在以下示例中，假定网页允许查看器的容器`DIV`占用Web浏览器窗口大小的40%。 而且，它的高度保持不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入的步骤类似。 唯一的区别是您无需显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入相同。 将容器`DIV`添加到现有`"holder"` `DIV`中。 以下代码是一个完整的示例。 请注意调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```
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

以下示例页面说明了在不限制高度的情况下响应式设计嵌入的更多实际用途：

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**定义宽度和高度的灵活大小嵌入**

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 它为`"holder"` DIV提供两种大小，并将其居中在浏览器窗口中。 此外，网页还将`HTML`和`BODY`元素的大小设置为100%。

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

其余的嵌入步骤与无限制高度的响应式嵌入步骤完全相同。 结果示例如下：

```
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

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和无目标构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会使用任何参数，并且配置参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例说明如何将固定大小嵌入与基于setter的API结合使用：

```
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

