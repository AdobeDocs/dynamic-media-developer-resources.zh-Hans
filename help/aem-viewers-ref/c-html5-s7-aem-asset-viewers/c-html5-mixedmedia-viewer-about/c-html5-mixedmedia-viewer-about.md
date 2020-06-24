---
description: 混合媒体查看器是媒体查看器。 它支持包含图像、样本集、旋转集、视频和自适应视频集的媒体集。
keywords: responsive
seo-description: 混合媒体查看器是媒体查看器。 它支持包含图像、样本集、旋转集、视频和自适应视频集的媒体集。
seo-title: 混合媒体
solution: Experience Manager
title: 混合媒体
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2681'
ht-degree: 0%

---


# 混合媒体{#mixed-media}

混合媒体查看器是媒体查看器。 它支持包含图像、样本集、旋转集、视频和自适应视频集的媒体集。

查看器底部的缩略图表示每个媒体集元素及其资产类型指示符。 选择样本集元素后，将显示第二行样本，以允许在样本集内选择颜色变化。 图像和样本集元素支持连续或内联模式的缩放； 旋转集支持缩放和旋转。 视频和自适应视频集支持所有基本的播放控件，只要视频内容顶部显示任何可选的隐藏式字幕。 用户可随时单击全屏按钮切换为全屏。 查看器具有可选的关闭按钮。 它设计为可在桌面和移动设备上使用。

当基础系统支持HLS格式的HTML5流视频回放时，混合媒体查看器在其默认配置中使用HLS格式。 在不支持HTML5流的系统上，查看器返回到HTML5渐进式视频投放。

>[!NOTE]
>
>此查看器不支持使用IR（图像渲染）或UGC（用户生成的内容）的图像。

查看器类型505。

请参 [阅系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## 使用混合媒体查看器 {#section-f21ac23d3f6449ad9765588d69584772}

混合媒体查看器表示主JavaScript文件和一组帮助文件（单个JavaScript包含该特定查看器、资源、CSS使用的所有查看器SDK组件），该查看器在运行时下载。

您可以使用随IS-Viewers提供的生产就绪型HTML页面，在弹出模式下使用混合媒体查看器。 或者，您可以在嵌入式模式下使用查看器，在该模式下，查看器会使用文档化的API集成到目标网页中。

配置查看器和设置查看器外观的任务与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参 [阅所有查看器的通用命令参考——所有查看器](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[的通用配置属性和通用命令参考- URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与混合媒体查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

混合媒体查看器支持其他移动应用程序中常见的单触和多触手势。 当查看器无法处理用户的轻扫手势时，它将事件转发到Web浏览器以执行本机页面滚动。 即使查看器占据了设备屏幕的大部分区域，用户也可通过此功能在页面中导航。

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
   <td colname="col2"> <p> 激活弹出视图或在主缩放级别和辅助缩放级别之间进行更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>多次点按 </p> </td> 
   <td colname="col2"> <p>在连续 <span class="codeph"> 缩 </span> 放模式下，放大一个级别，直到达到最大放大率，下一个多次点击手势将重置为初始状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>触摸并按住 </p> </td> 
   <td colname="col2"> <p> 在内联缩 <span class="codeph"> 放模 </span> 式下，激活缩放的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>在连续缩放模式下，放大或缩小图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 当当前资产是旋转集，并且图像处于重置状态时，它将水平旋转旋转旋转集。 </p> <p> 当当前资产是旋转集或图像，且图像被放大时，它将水平移动图像。 如果图像被移到视图边缘，并且仍沿该方向轻扫，则手势将执行本机页面滚动。 </p> <p> 滚动浏览色板条中色板的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直轻扫或轻扫 </p> </td> 
   <td colname="col2"> <p> 如果图像处于重置状态，则在使用多维旋转集时，图像会更改垂直视图角。 在一维旋转集中，或者当多维旋转集位于最后一个或第一个轴上时，如果垂直轻扫不会导致垂直视图角度发生变化，则手势将执行本机页面滚动。 </p> <p> 当当前资产是旋转集或图像，且图像放大后，垂直移动图像。 如果图像被移到视图边缘，并且仍沿该方向轻扫，则手势将执行本机页面滚动。 </p> <p> 如果手势是在色板区域内完成的，它将执行本机页面滚动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

查看器还支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器完全可通过键盘访问。

请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 嵌入混合媒体查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看器行为有不同的需求。 有时网页会提供链接，单击该链接后，将在单独的浏览器窗口中打开查看器。 在其他情况下，必须将查看器直接嵌入到托管页面中。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上或针对不同的浏览器窗口大小显示不同。 为满足这些需求，查看器支持三种主要操作模式： 弹出窗口、固定大小嵌入和响应式设计嵌入。

## 关于弹出模式 {#section-77d5aa03b8b94566958a179b1a2cd474}

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或移动设备的方向更改时进行调整。

弹出模式是移动设备中最常见的模式。 网页使用JavaScript调用、正确 `window.open()` 配置的HTML元素或任 `A` 何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 在这种情况下，它被调 [!DNL MixedMediaViewer.html] 用并位于标准IS [!DNL html5/] 查看器部署的子文件夹中：

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

通过应用自定义CSS，可以实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 关于固定大小和响应式设计嵌入 {#section-ec86b100ba5943d0b16694268520bbde}

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常只占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，还有响应式设计页面，可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，将使用固定大小嵌入。 这是具有静态布局的网页的最佳选择。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器的大小变化 `DIV`。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式取决于网页调整其容器的方式 `DIV`。 如果网页仅设置容器的宽度，而 `DIV`保持高度不受限制，则查看器会根据所使用的资产的长宽比自动选择其高度。 此功能可确保资产完美地适合视图，而不会在两侧添加任何边距。 此用例是使用响应式设计布局框架(如Bootstrap、基础等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器的宽度和高度，则查看器仅填充该区域 `DIV`，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模态叠加中，其中叠加根据Web浏览器窗口大小进行大小调整。

## 固定大小嵌入 {#section-17d162f76ffa4804b27928f51e7bea1d}

通过执行以下操作，可将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含该查看器 [!DNL MixedMediaViewer.js]。 文 [!DNL MixedMediaViewer.js] 件位于标准IS [!DNL html5/js/] 查看器部署的子文件夹下：

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

如果查看器部署在某个Adobe Scene7服务器上，并且来自同一域，则可以使用相对路径。 否则，您将指定一个指向已安装IS-Viewer的Adobe Scene7服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主 `include` 查看器JavaScript文件。 在网页代码中不应引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 尤其不要直接引用查看器从上 `Utils.js` 下文路径加载的 `/s7viewers` HTML5 SDK库(所谓的统一SDK `include`)。 原因在于查看器的逻辑 `Utils.js` 完全管理或类似运行时查看器库的位置，并且查看器版本之间的位置会发生变化。 Adobe不会在服务器上保留旧版本的 `includes` 辅助查看器。
>
>
>因此，在页面上直接引用查看器使 `include` 用的任何辅助JavaScript会在将来部署新产品版本时破坏查看器功能。

1. 定义容器DIV。

   将空DIV元素添加到要显示查看器的页面。 DIV元素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是定位的元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`。

   确保全屏功能在Internet Explorer中正常工作。 检查以确保DOM中没有其他元素的堆叠顺序高于占位符DIV。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. 设置查看器大小

   此查看器在处理多项目集时显示缩略图。 在桌面系统上，缩略图放在主视图下。 同时，查看器允许在运行时使用API交换主资 `setAsset()` 产。 作为开发人员，您可以控制当新资产只有一个项目时查看器管理底部缩略图区域的方式。 可以保持外部查看器的大小不变，并让主视图增加其高度并占用缩略图区域。 或者，您可以保持主视图大小为静态并折叠外部查看器区域，让网页内容向上移动，然后使用缩略图中留下的免费页面空间。

   要保持外部查看器边界不变，请以绝 `.s7mixedmediaviewer` 对单位定义顶级CSS类的大小。 CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配到Scene7 Publishing System中的查看器预设记录，或使用样式命令显式传递。

   有关 [使用CSS设置查看器样式](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) ，请参阅自定义混合媒体查看器。

   以下是在HTML页面中定义静态外部查看器大小的示例：

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在以下示例页面上查看具有固定外部查看器区域的行为。 请注意，在集之间切换时，外部查看器大小不会更改：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   要使主视图维保持静态，请使用CSS选择器或使用修饰符，以内部SDK组 `Container` 件的绝对 `.s7mixedmediaviewer .s7container` 单位定义查看器 `stagesize` 大小。

   以下是为内部SDK组件定义查看器大 `Container` 小的示例，以便在切换资产时主视图区域不更改其大小：

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   以下示例页显示具有固定主视图大小的查看器行为。 请注意，在集之间切换时，主视图将保持静态，网页内容将垂直移动：

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   您可以在Scene7 Publishing `stagesize``params` System的查看器预设记录中设置修饰符，或将其与查看器初始化代码与集合显式传递，或作为API调用（如本帮助的“命令参考”部分所述）进行传递，如下所示：

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建类的一个实例，将 `s7viewers.MixedMediaViewer` 所有配置信息传递给它的构造函数，并在查看器实例 `init()` 上调用方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有包含查 `containerId` 看器容器ID名称的字段，以及包含查看器支持 `params` 的配置参数的嵌套JSON对象。 在这种情况下，对 `params` 象必须至少将图像服务URL作为属性传 `serverUrl` 递，将视频服务器URL作为属性传递， `videoserverurl` 将初始资产作为参 `asset` 数传递。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码能够按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为获得最大兼容性， `init()` 请在结束标签之前或 `BODY` 在正文事件上调用方 `onload()` 法。

   同时，容器元素不一定是网页布局的一部分。 例如，使用分配给它的样 `display:none` 式可能会隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 出现这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例、将最小必要配置选项传递给构造函数并调用方法的示 `init()` 例。 该示例假 `mixedMediaViewer` 定是查看器实例； `s7viewer` 是占位符的名称 `DIV`; [!DNL http://s7d1.scene7.com/is/image/] 是图像服务URL; [!DNL http://s7d1.scene7.com/is/content/] 是视频服务器URL; 而 [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] 是资产：

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

以下代码是嵌入具有固定大小的混合媒体查看器的普通网页的完整示例：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 具有无限制高度的响应式嵌入 {#section-056cb574713c4d07be6d07cf3c598839}

通过响应式设计嵌入，网页通常具有某种灵活的布局，这些布局决定了查看器容器的运行时大小 `DIV`。 在以下示例中，假定网页允许查看者的容器占Web浏 `DIV` 览器窗口大小的40%，同时保持其高度不受限制。 网页HTML代码如下所示：

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

上述所有步骤与固定大小嵌入相同。 将容器DIV添加到现有 `"holder"` DIV。 下面的代码是一个完整的示例。 注意调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下示例页面说明了在不限制高度的情况下响应式设计嵌入的更多实际用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## 定义宽度和高度的灵活大小嵌入 {#section-0a329016f9414d199039776645c693de}

如果定义了宽度和高度的灵活大小嵌入，则网页样式会有所不同。 它为DIV提供两种大 `"holder"` 小，并将其居中在浏览器窗口中。 此外，网页会将元素和元素的 `HTML` 大小 `BODY` 设置为100%。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 使用基于Setter的API进行嵌入 {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

可以使用基于setter的API和无目标构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不会采用任何参数，并且配置参数是使用、 `setContainerId()`和 `setParam()`API方法 `setAsset()` 指定的，并单独调用JavaScript。

以下示例说明如何将固定大小嵌入与基于setter的API结合使用：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

