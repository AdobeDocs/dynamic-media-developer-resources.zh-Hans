---
description: eCatalog Viewer是一个目录查看器，它以跨页或逐页的方式显示电子小册子。eCatalog允许用户使用其他用户界面元素或专用缩略图模式浏览目录。 用户还可以放大每个页面，获得更详细的信息。
keywords: 响应
solution: Experience Manager
title: eCatalog
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2174'
ht-degree: 0%

---


# eCatalog{#ecatalog}

eCatalog Viewer是一个目录查看器，它以跨页或逐页的方式显示电子小册子。eCatalog允许用户使用其他用户界面元素或专用缩略图模式浏览目录。 用户还可以放大每个页面，获得更详细的信息。

>[!NOTE]
>
>此查看器不支持使用图像渲染(IR)或用户生成内容(UGC)的图像。

查看器类型507。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

此查看器可使用电子目录，并支持可选的图像映射和社交共享工具。 它具有缩放工具、目录导航工具、全屏支持、缩略图和可选的关闭按钮。 查看器还支持社交共享工具、打印、下载和收藏夹。 它设计为可在桌面和移动设备上使用。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## 使用eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Viewer表示主JavaScript文件和一组帮助文件（单个JavaScript包含在由查看器在运行时下载的由此特定查看器、资源、CSS使用的所有查看器SDK组件中）

您可以使用随IS-Viewer提供的生产就绪型HTML页面，在弹出模式下使用eCatalog Viewer，或在嵌入模式下(在嵌入模式下，它使用文档化的API集成到目标网页中)使用。

配置和外观设置与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅所有查看器的通用命令参考 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看器通用的通用命令参考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[[

## 与eCatalog Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}交互

eCatalog Viewer支持其他移动应用程序中常见的以下触控手势。

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
   <td colname="col2"> <p> 在色板中选择新缩览图。 </p> </td> 
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
   <td colname="col2"> <p> 如果使用幻灯片框架过渡，则滚动浏览目录页的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫或轻击 </p> </td> 
   <td colname="col2"> <p>当图像处于重置状态时，将执行本机页面滚动。 </p> <p>当缩览图处于活动状态时，将滚动缩览图的列表。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以启用逼真的页面翻转动画效果以在目录页面之间导航。 在这种情况下，用户可以按住并拖动页面角并翻转页面。

此查看器还支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器完全可通过键盘访问，如[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)中所述。

## 使用eCatalog Viewer {#section-eb575084a99647c3a9591f439f40b412}的社交媒体共享工具

eCatalog查看器支持社交共享工具。这些工具可用作主控件栏中的按钮，当用户单击或点按时，该按钮将扩展到共享工具栏。

共享工具栏包含支持的每种共享渠道类型的图标，包括Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个带有相应数据输入表单的模态对话框。 调用Facebook或Twitter时，查看器会将用户从社交服务重定向到标准共享对话框。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入eCatalog查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看器行为有不同的需求。 有时网页会提供一个链接，单击该链接后，将在单独的浏览器窗口中打开查看器。 在其他情况下，必须将查看器直接嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上或针对不同浏览器窗口大小显示不同。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或移动设备的方向更改时进行调整。

弹出模式是移动设备最常见的模式。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 在这种情况下，它称为[!DNL eCatalogViewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹中：

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

您可以通过应用自定义CSS实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常仅占据网页的一部分空间。

主要用例是面向桌面或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 对于具有静态布局的网页，这是最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页大小其容器`DIV`的方式而异。 如果网页仅设置容器的宽度`DIV`，而保持高度不受限，则查看器会根据所使用资产的宽高比自动选择其高度。 此功能可确保资产完美适合视图，且两侧无填充。 此用例是使用响应式布局框架(如Bootstrap、Foundation等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个不错的示例是将查看器嵌入到模式叠加中，其中的叠加会根据Web浏览器窗口大小进行调整。

**固定大小嵌入**

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标签。 在使用查看器API之前，请确保包含[!DNL eCatalogViewer.js]。 [!DNL eCatalogViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并从同一域提供，则可以使用相对路径。 否则，您将指定一个指向安装了IS-Viewer的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
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

1. 设置查看器大小

   您可以通过以下两种方式设置查看器的静态大小：以绝对单位为`.s7ecatalogviewer`顶级CSS类声明查看器，或使用`stagesize`修饰符。

   您可以将大小调整直接放在CSS中的HTML页面上，或放在自定义查看器CSS文件中，该文件稍后会在Dynamic Media Classic中分配给查看器预设记录，或使用样式命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义eCatalog查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)。

   以下是在HTML页中定义静态查看器大小的示例：

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic的查看器预设记录中设置`stagesize`修饰符，或将其显式传递给带有`params`集合的查看器初始化代码，或作为“命令参考”部分中所述的API调用进行传递，如下所示：

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. 正在初始化查看器。

   完成上述步骤后，您将创建`s7viewers.eCatalogViewer`类的实例，将所有配置信息传递给它的构造函数，并对查看器实例调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少具有`containerId`字段，该字段包含查看器容器ID的名称以及查看器支持的配置参数嵌套的`params` JSON对象。 在这种情况下，`params`对象必须至少具有作为`serverUrl`属性传递的图像服务URL，以及作为`asset`参数传递的初始资产。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会将构建DOM延迟到网页结束。 但是，要获得最大兼容性，请在结束`BODY`标签之前或在正文`onload()`事件上调用`init()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可能会使用分配给它的`display:none`样式将其隐藏。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例、将最少的必要配置选项传递给构造函数并调用`init()`方法的示例。 该示例假定`eCatalogViewer`为查看器实例；`s7viewer`是占位符`DIV`的名称；`http://s7d1.scene7.com/is/image/`是图像服务URL，`Viewers/Pluralist`是资产：

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是嵌入具有固定大小的eCatalog查看器的次要网页的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，指示查看器容器的运行时大小`DIV`。 为本示例之目的，假定网页允许查看器的容器`DIV`采用Web浏览器窗口大小的40%，同时保持其高度不受限制。 生成的网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入类似，唯一的区别是您无需显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

以上步骤与固定大小嵌入相同。 将容器`DIV`添加到现有的&quot; holder&quot; `DIV`。 以下代码是一个完整的示例。 您可以查看调整浏览器大小时查看器大小的更改方式，以及查看器长宽比与资产的匹配方式。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页说明了具有无限高度的响应式设计嵌入的更多实际使用案例：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

**定义了宽度和高度的灵活大小嵌入**

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 也就是说，它为“holder” `DIV`提供两种大小，并将其居中在浏览器窗口中。 此外，网页会将`HTML`和`BODY`元素的大小设置为100%:

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

其余的嵌入步骤与无限制高度的响应式设计嵌入相同。 结果示例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API构造函数不会使用任何参数，而且配置参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

以下示例显示了具有基于setter的API的固定大小嵌入：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```

