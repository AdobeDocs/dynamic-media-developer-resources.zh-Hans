---
description: eCatalog Viewer是一个目录查看器，它通过跨页或逐页显示电子小册子，通过eCatalog，用户可以使用其他用户界面元素或专用缩略图模式在目录中导航。 用户还可以放大每个页面，以获得更详细的信息。
keywords: responsive
seo-description: eCatalog Viewer是一个目录查看器，它通过跨页或逐页显示电子小册子，通过eCatalog，用户可以使用其他用户界面元素或专用缩略图模式在目录中导航。 用户还可以放大每个页面，以获得更详细的信息。
seo-title: eCatalog
solution: Experience Manager
title: eCatalog
topic: Dynamic media
uuid: 6950306d-637e-4932-ae96-c5366e5477f3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# eCatalog{#ecatalog}

eCatalog Viewer是一个目录查看器，它通过跨页或逐页显示电子小册子，通过eCatalog，用户可以使用其他用户界面元素或专用缩略图模式在目录中导航。 用户还可以放大每个页面，以获得更详细的信息。

>[!NOTE]
>
>此查看器不支持使用图像渲染(IR)或用户生成内容(UGC)的图像。

查看器类型507。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

此查看器可与电子目录一起使用，并支持可选的图像映射和社交共享工具。 它具有缩放工具、目录导航工具、全屏支持、缩略图和可选的关闭按钮。 查看器还支持社交共享工具、打印、下载和收藏夹。 它设计为可在桌面和移动设备上使用。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## 使用eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog Viewer表示主JavaScript文件和一组帮助文件（单个JavaScript包含查看器SDK组件，该查看器在运行时下载该特定查看器、资源、CSS所使用的所有查看器SDK组件）

您可以在弹出模式下使用随IS查看器提供的生产就绪型HTML页面，或在嵌入式模式下使用eCatalog查看器，在该模式下，eCatalog查看器使用文档化的API集成到目标网页中。

配置和外观设置与其他查看器的配置和外观设置类似。 所有外观设计都通过自定义CSS实现。

请参 [阅所有查看器通用的命令参考——所有查看器通用的配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令参考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与eCatalog Viewer交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

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
   <td colname="col2"> <p> 放大一个级别，直到达到最大放大率。 下一个多次点按手势将查看器重置为初始查看状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或缩小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 如果使用幻灯片框架列表，则滚动浏览目录页面过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p>当图像处于重置状态时，它将执行本机页面滚动。 </p> <p>当缩略图处于活动状态时，它将滚动缩略图的列表。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以启用逼真的页面翻转动画效果，以便在目录页面之间导航。 在这种情况下，用户可以按住并拖动页面角并翻转页面。

此查看器还支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

按键盘辅助功能和导航中所述，此查看器可 [以完全通过键盘访问](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用eCatalog Viewer的社交媒体共享工具 {#section-eb575084a99647c3a9591f439f40b412}

eCatalog查看器支持社交共享工具。这些工具可作为主控件栏中的按钮使用，当用户单击或点按时，该按钮会扩展到共享工具栏中。

共享工具栏包含支持的每种共享渠道类型的图标，包括Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个模态对话框，其中包含相应的数据输入表单。 调用Facebook或Twitter时，查看器会从社交服务将用户重定向到标准共享对话框。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入eCatalog查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看器行为的需求不同。 有时，网页会提供一个链接，单击该链接后，将在单独的浏览器窗口中打开查看器。 在其他情况下，必须将查看器直接嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同的内容，或针对不同的浏览器窗口大小显示不同的内容。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或移动设备的方向更改时进行调整。

弹出模式是移动设备最常见的模式。 网页使用 `window.open()` JavaScript调用、正确配置的 `A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 在这种情况下，它被调用， [!DNL eCatalogViewer.html] 并位于标准IS查看 [!DNL html5/] 器部署的子文件夹中：

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

您可以通过应用自定义CSS实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式中，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常只占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器的大小变化 `DIV`。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页调整其容器的方式而异 `DIV`。 如果网页仅设置容器的宽度，并且高度不受限制，则查看器会根据所使用的资产的长宽比自动选择其高度。 `DIV`此功能可确保资产完美适合视图，且两侧没有填充。 此用例是使用响应式布局框架（如Bootstrap、Foundation等）的网页中最常见的用例。

否则，如果网页同时设置查看器容器的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 `DIV`一个很好的示例是将查看器嵌入到模态叠加中，其中叠加根据Web浏览器窗口大小进行大小调整。

**固定大小嵌入**

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含该查看器 [!DNL eCatalogViewer.js]。 该文 [!DNL eCatalogViewer.js] 件位于标准IS查看 [!DNL html5/js/] 器部署的子文件夹下：

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并且从同一域提供该查看器，则可以使用相对路径。 否则，您将指定一个安装了IS查看器的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查 `include` 看器JavaScript文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用查看器从上下文路 `Utils.js` 径加载的HTML5 SDK库( `/s7viewers` 所谓的统一SDK `include`)。 原因在于，查看器的逻辑可 `Utils.js` 以完全管理或类似运行时查看器库的位置，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的 `includes` 辅助查看器。
>
>
>因此，在页面上直接引用查看器使用的任 `include` 何辅助JavaScript会在将来部署新产品版本时破坏查看器功能。

1. 定义容器DIV。

   将空DIV元素添加到要显示查看器的页面。 DIV元素必须定义其ID，因为此ID稍后会传递到查看器API。

   占位符DIV是定位的元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   可以通过以绝对单位声明顶级CSS类的查看器，或 `.s7ecatalogviewer` 者使用修饰符来设置查看器的静态 `stagesize` 大小。

   您可以将大小调整直接放在HTML页面上，或放在自定义查看器CSS文件中，该文件稍后会分配到Scene7 Publishing System中的查看器预设记录，或使用样式命令显式传递。

   有关使 [用CSS设置查看器样式的更多信息](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) ，请参阅自定义eCatalog查看器。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Scene7 Publishing System的查看器预设记录中设置修饰符，或将修饰符与查看器初始化代码显式传递给集合，或者作为“命令参考”部分中所述的API调用进行传递，如下所示： `stagesize``params`

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. 初始化查看器。

   完成上述步骤后，您将创建类的一个实例，将所有配置信息传递给它的构造函数，并对查看器实例 `s7viewers.eCatalogViewer``init()` 调用方法。 配置信息作为JSON对象传递给构造函数。 此对象至少包含一个字段， `containerId` 该字段包含查看器容器ID的名称以及查看器支持的配置参数的嵌套 `params` JSON对象。 在这种情况下，对 `params` 象必须至少将图像服务URL作为属性传递， `serverUrl` 并将初始资产作为参 `asset` 数。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码能够按其ID找到容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 但是，要获得最大兼容性，请 `init()` 在结束标签之前或在正 `BODY` 文事件上调用方 `onload()` 法。

   同时，容器元素不一定是网页布局的一部分。 例如，可能会使用分配给它的样 `display:none` 式来隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例的示例，将最小必要的配置选项传递给构造函数并调用方 `init()` 法。 示例假定 `eCatalogViewer` 是查看器实例；是 `s7viewer` 占位符的名称 `DIV`;是图 `http://s7d1.scene7.com/is/image/` 像服务URL, `Viewers/Pluralist` 也是资产：

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

   以下代码是嵌入具有固定大小的eCatalog查看器的简单网页的完整示例：

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

通过响应式设计嵌入，网页通常具有某种灵活的布局，它决定了查看器容器的运行时大小 `DIV`。 就本示例而言，假定网页允许查看者的容器占Web浏览器窗口大小的40%，并保持其高度不受限制。 `DIV` 生成的网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入类似，唯一的区别在于您无需显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

以上所有步骤与固定大小嵌入相同。 将容器添 `DIV` 加到现有的“持有人” `DIV`。 以下代码是一个完整的示例。 您可以查看调整浏览器大小时查看器大小的更改方式，以及查看器长宽比与资产的匹配方式。

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

[https://marketing.adobe.com/resources/help/zh_CN/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**定义宽度和高度的灵活大小嵌入**

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 即，它向“holder”提供两种大小，并将 `DIV` 其居中在浏览器窗口中。 此外，网页会将元素和元素的大 `HTML` 小设 `BODY` 置为100%:

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

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API构造函数时，不会使用任何参数，并且配置参数是使用 `setContainerId()`、 `setParam()`和 `setAsset()` API方法指定的，这些方法具有单独的JavaScript调用。

以下示例显示了使用基于setter的API进行固定大小嵌入：

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

