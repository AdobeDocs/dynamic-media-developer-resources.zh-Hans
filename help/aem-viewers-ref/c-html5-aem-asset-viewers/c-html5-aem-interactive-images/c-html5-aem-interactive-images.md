---
title: 交互式图像
description: 交互式图像查看器是一种查看器，它显示单个不可缩放的图像，其中包含可单击的热点。 此查看器旨在实施“可购物横幅”体验。 也就是说，用户可以在横幅图像上选择一个热点，并重新定向到您网站上的概览或产品详细信息页面。 它设计为可在台式机和移动设备上工作。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# 交互式图像{#interactive-image}

交互式图像查看器是一种查看器，它显示单个不可缩放的图像，其中包含可单击的热点。 此查看器旨在实施“可购物横幅”体验。 也就是说，用户可以在横幅图像上选择一个热点，并重新定向到您网站上的概览或产品详细信息页面。 它设计为可在台式机和移动设备上工作。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型为508。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

参见 [系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 使用交互式图像查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

交互式图像查看器表示一个主JavaScript文件和一组帮助文件（单个JavaScript包含由此特定查看器使用的所有Viewer SDK组件、资产、CSS），这些文件由查看器在运行时下载。

交互式图像查看器只能在嵌入式模式下使用，在该模式下，它使用文档记录的API集成到目标网页中。

配置和外观设计类似于本帮助中描述的其他查看器。 所有外观设计都是通过自定义CSS实现的。

参见 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与交互式图像查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

视频图像查看器支持的交互是桌面系统上的热点激活。 此激活发生在点击和点按触控设备上。

查看器完全可使用键盘。

参见 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入交互式图像查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

交互式图像查看器将嵌入到托管页面中。 这样的网页可以具有静态布局，或者它可以“响应”并且在不同设备或不同浏览器窗口大小上以不同的方式显示。

为了满足这些需求，查看器支持两种主要操作模式：固定大小嵌入和响应式嵌入。

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入式模式下，查看器将添加到现有网页中。 此网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占用网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 对于具有静态布局的网页，此方法为最佳选择。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器的大小更改 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页确定其容器大小的方式 `DIV`. 如果网页仅设置容器的宽度 `DIV`如果不限制高度，查看器会根据所用资源的纵横比自动选择高度。 此功能可确保资源完全适合视图，而不用填充边距。 此用例最常用于使用响应式Web设计布局框架(如Bootstrap和Foundation)的网页。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器会填充该区域。 它还遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要您在HTML头中添加脚本标记。 在使用查看器API之前，请确保包括 [!DNL InterativeImage.js]. 此 [!DNL InteractiveImage.js] 文件位于 [!DNL html5/js/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

如果查看器部署在一台Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，请指定已安装IS-Viewers的某个Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件。 请勿在网页代码中引用任何可能由查看器的逻辑在运行时下载的其他JavaScript文件。 特别是，请勿直接引用HTML5 SDK `Utils.js` 由查看器加载的库，从 `/s7viewers` 上下文路径（所谓的整合SDK） `include`)。 原因在于 `Utils.js` 或类似的运行时查看器库完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不保留辅助查看器的旧版本 `includes` 在服务器上。
>
>
>因此，直接引用任何辅助JavaScript `include` 将来部署新产品版本时，页面上查看器使用的功能会中断查看器。

1. 定义容器 `DIV`.

   添加空 `DIV` 元素到您希望查看器显示的页面。 此 `DIV` 元素必须定义其ID，因为此ID稍后会被传递到查看器API。 DIV的大小通过CSS指定。

   占位符 `DIV` 是一个定位元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   以下是定义的占位符示例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   通过声明查看器的静态大小，可以将其设置为 `.s7interactiveimage` 以绝对单位表示的顶级CSS类，或者使用 `stagesize` 修饰符。

   您可以直接在“HTML”页面上设置CSS大小。 或者，您可以将大小调整放入自定义查看器CSS文件中，该文件随后将分配给Adobe Experience Manager Assets中的查看器预设记录（按需），或者使用进行明确传递 `style` 命令。

   参见 [视频](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 有关使用CSS为查看器设置样式的更多信息。

   以下是在“HTML”页中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   您可以明确地传递 `stagesize` 修饰符，查看器初始化代码为 `params` 收藏集或作为API调用，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   建议使用基于CSS的方法，并用于此示例。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.InteractiveImage` 类，将所有配置信息传递到其构造函数，并调用 `init()` 方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有 `containerId` 保存查看器容器ID名称并嵌套的字段 `params` 具有查看器支持的配置参数的JSON对象。 在本例中， `params` 对象必须至少将图像服务URL传递为 `serverUrl` 资产，而初始资产为 `asset` 参数。 基于JSON的初始化API允许您使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大的兼容性，请调用 `init()` 紧靠结束位置之前的方法 `BODY` 标签上，或正文上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可使用以下方式隐藏该内容： `display:none` 为其分配的样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 发生此事件时，查看器加载会自动恢复。

   以下示例介绍了如何创建查看器实例，将最低必要的配置选项传递给构造函数并调用 `init()` 方法。 此示例假定 `interactiveImage` 是查看器实例； `s7viewer` 是占位符的名称 `DIV`； `http://aodmarketingna.assetsadobe.com/is/image` 是图像服务URL，并且 `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` 是资产：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   以下代码是一个简单网页的完整示例，该网页以固定大小嵌入视频图像查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器的运行时大小 `DIV`. 对于以下示例，假设网页允许查看器的容器 `DIV` 以获得Web浏览器窗口大小的40%。 而且高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入的步骤类似。 唯一的区别是，您不需要显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 创建和初始化查看器。

上述所有步骤与固定大小的嵌入步骤相同。 添加容器 `DIV` 到现有 `"holder"` `DIV`. 以下代码是一个完整的示例。 请注意浏览器调整大小时查看器大小的变化情况，以及查看器长宽比与资源的匹配情况。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下示例页面说明了高度不受限制的响应式设计嵌入的更多实际用途：

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**定义宽度和高度的灵活大小嵌入**

如果定义了宽度和高度的灵活大小嵌入，则网页的样式会不同。 它将两种大小提供给 `"holder"` 在浏览器窗口中进行DIV和居中对齐。 此外，该网页还设置 `HTML` 和 `BODY` 元素为100%。

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

其余嵌入步骤与用于高度不受限制的响应式嵌入的步骤相同。 产生的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不接受任何参数，并且配置参数是使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法具有单独的JavaScript调用。

以下示例说明了如何将固定大小嵌入与基于setter的API结合使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
