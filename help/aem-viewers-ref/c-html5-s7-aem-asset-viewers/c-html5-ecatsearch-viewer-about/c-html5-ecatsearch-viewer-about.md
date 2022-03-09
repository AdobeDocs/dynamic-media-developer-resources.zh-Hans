---
description: eCatalog搜索查看器是一种目录查看器，它以跨页或逐页的方式显示电子小册子。eCatalog允许用户使用其他用户界面元素或专用缩略图模式浏览目录。 用户还可以放大每个页面，以了解更多详细信息。
keywords: 响应式
solution: Experience Manager
title: 电子目录搜索
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# 电子目录搜索{#ecatalog-search}

eCatalog搜索查看器是一种目录查看器，它以跨页或逐页的方式显示电子小册子。eCatalog允许用户使用其他用户界面元素或专用缩略图模式浏览目录。 用户还可以放大每个页面，以了解更多详细信息。

此查看器可与电子目录结合使用，并支持可选的图像映射和社交共享工具。 它具有缩放工具、目录导航工具、全屏支持、缩略图和可选的关闭按钮。 查看器还支持社交共享工具、打印、下载和收藏。 它适用于台式机和移动设备。

用户还可以对目录内容进行基于关键字或基于短语的搜索。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型513。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## 使用eCatalog查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog搜索查看器表示主JavaScript文件以及查看器在运行时下载的一组帮助程序文件(单个JavaScript包含该查看器的所有查看器SDK组件，这些组件由该特定查看器（资产、CSS）使用)

您可以在弹出模式下使用eCatalog搜索查看器，它使用随IS查看器提供的生产就绪HTML页面，或在嵌入式模式下使用，在嵌入式模式下，eCatalog搜索查看器可使用记录在案的API集成到目标网页中。

配置和外观设置与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器 — URL通用的命令引用](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与eCatalog搜索查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog搜索查看器支持其他移动设备应用程序中常见的以下触控手势。

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
   <td colname="col2"> <p> 在色板中选择新的缩略图。 </p> </td> 
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
   <td colname="col2"> <p>如果使用幻灯片框架过渡，则滚动浏览目录页面列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p>当图像处于重置状态时，将执行本机页面滚动。 </p> <p>当缩略图处于活动状态时，将滚动缩略图列表。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以启用逼真的页面翻转动画效果，以便在目录页面之间导航。 在这种情况下，用户可以按住并拖动页面角并翻转页面。

此查看器还支持在具有触摸屏和鼠标的Windows设备上输入触摸输入和鼠标。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

## 使用eCatalog搜索查看器共享社交媒体工具 {#section-eb575084a99647c3a9591f439f40b412}

eCatalog搜索查看器支持社交共享工具。这些工具可用作主控制栏中的按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏包含支持的每种类型共享渠道的图标，其中包括Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个包含相应数据输入表单的模式对话框。 调用Facebook或Twitter时，查看器会将用户从社交服务重定向到标准共享对话框。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

查看器的“搜索”功能在主工具栏中以玻璃图标的形式提供。 单击或点按该图标可激活带有输入字段的“搜索”面板。 在输入关键词或短语并按Enter后，查看器会在面板中呈现搜索结果并突出显示主视图中的找到的单词。

## 嵌入eCatalog搜索查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时，网页会提供一个链接，在选定该链接后，该链接会在单独的浏览器窗口中打开查看器。 在其他情况下，需要将查看器权限嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或移动设备方向发生更改时进行调整。

弹出模式是移动设备最常见的模式。 网页使用 `window.open()` JavaScript调用，已正确配置 `A` HTML元素，或任何其他合适的方法。

建议您使用现成的HTML页面进行弹出操作模式。 在这种情况下，它称为 [!DNL eCatalogSearchViewer.html] 和位于 [!DNL html5/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占据网页的一部分房地产。

主要用例包括面向台式机或平板电脑设备的网页，以及响应式设计的页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器的大小变化 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式与网页大小其容器的方式有所不同 `DIV`. 如果网页仅设置容器的宽度 `DIV`，查看器会根据所使用资产的宽高比自动选择其高度，而不限制其高度。 此功能可确保资产完美地放入视图中，侧边无需任何内边距。 对于使用响应式布局框架(如Bootstrap、基础等)的网页，此用例最常见。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML头中添加脚本标记。 在使用查看器API之前，请确保在 [!DNL eCatalogSearchViewer.js]. 的 [!DNL eCatalogSearchViewer.js] 文件位于 [!DNL html5/js/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

如果查看器部署在其中一个Adobe的Dynamic Media服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装IS-Viewer的AdobeDynamic Media服务器的完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. 定义容器DIV。

   在希望查看器显示的页面中添加空DIV元素。 必须定义DIV元素的ID，因为此ID稍后会传递到查看器API。

   占位符DIV是放置元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 设置查看器大小

   您可以通过声明查看器的静态大小 `.s7ecatalogsearchviewer` 以绝对单位表示的顶级CSS类，或通过使用 `stagesize` 修饰符。

   您可以将大小调整直接放在CSSHTML页面上，或放在自定义查看器CSS文件中，该文件稍后会分配给Dynamic Media Classic中的查看器预设记录，或使用样式命令显式传递。

   请参阅 [自定义eCatalog查看器](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 有关使用CSS为查看器设置样式的更多信息。

   以下示例用于在HTML页面中定义静态查看器大小：

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以设置 `stagesize` 修改量(在Dynamic Media Classic的查看器预设记录中)，或使用查看器初始化代码(通过 `params` 集合，或作为API调用（如命令引用部分中所述），如下所示：

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. 初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.eCatalogSearchViewer` 类，将所有配置信息传递给其构造函数并调用 `init()` 方法。 配置信息作为JSON对象传递到构造函数。 此对象至少具有 `containerId` 包含查看器容器ID和嵌套名称的字段 `params` 具有查看器支持的配置参数的JSON对象。 在本例中， `params` 对象必须至少将图像服务URL作为 `serverUrl` 资产，初始资产则作为 `asset` 参数。 通过基于JSON的初始化API，您可以使用一行代码创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 但是，为了实现最大兼容，请调用 `init()` 方法 `BODY` 标记，或在主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用 `display:none` 样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此情况时，查看器加载会自动恢复。

   以下示例用于创建查看器实例，将最小必需的配置选项传递给构造函数，并调用 `init()` 方法。 该示例假定 `eCatalogSearchViewer` 为查看器实例； `s7viewer` 是占位符的名称 `DIV`; `https://s7d1.scene7.com/is/image/` 是图像提供URL， `Viewers/Pluralist` 是资产：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是嵌入具有固定大小的eCatalog搜索查看器的简单网页的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**具有无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指示查看器容器的运行时大小 `DIV`. 就本例而言，假定网页允许查看者的容器 `DIV` 可获取Web浏览器窗口大小的40%，从而使其高度不受限制。 生成的网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入类似，唯一的区别在于您不需要明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同。 添加容器 `DIV` 至现有“持有人” `DIV`. 以下代码是一个完整的示例。 您可以查看在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面展示了具有不受限制高度的响应式设计嵌入的更多真实用例：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

**定义宽度和高度的灵活大小嵌入**

在定义了宽度和高度的灵活大小嵌入时，网页样式会有所不同。 也就是说，它为“holder”提供两种大小 `DIV` 并将其居中在浏览器窗口中。 此外，网页还会设置 `HTML` 和 `BODY` 元素到100%:

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

其余嵌入步骤与具有无限制高度的响应式设计嵌入步骤相同。 结果示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 对于该API构造函数，不会获取任何参数，并且配置参数是使用 `setContainerId()`, `setParam()`和 `setAsset()` 包含单独JavaScript调用的API方法。

以下示例显示了使用基于setter的API进行固定大小嵌入的示例：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
