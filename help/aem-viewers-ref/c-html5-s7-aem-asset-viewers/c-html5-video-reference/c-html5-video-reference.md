---
title: 视频
description: 视频查看器是一个视频播放器，可播放以H.264格式编码的流视频和渐进式视频。 它由Dynamic Media Classic或Adobe Experience Manager与Dynamic Media一起提供。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2372'
ht-degree: 0%

---

# 视频{#video}

视频查看器是一个视频播放器，可播放以H.264格式编码的流视频和渐进式视频。 它是从Dynamic Media Classic提供的，或与Dynamic Media一起提供的Experience Manager。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

同时支持单个视频集和自适应视频集。 此外，查看器还支持使用在外部位置托管的渐进式视频流和HLS流。 它可同时在支持HTML5视频的桌面和移动Web浏览器上使用。 此查看器还支持视频内容、视频章节导航和社交媒体共享工具顶部显示的可选隐藏式字幕。

当基础系统支持HTML5时，视频查看器在其默认配置中使用HLS格式的视频流播放。 在不支持HTML5流播放的系统上，查看器返回到HTML5渐进式视频交付。

查看器类型506。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用视频查看器 {#section-f21ac23d3f6449ad9765588d69584772}

视频查看器表示一个主JavaScript文件和一组帮助程序文件 — 单个JavaScript包含该查看器的所有查看器SDK组件，这些组件由该查看器在运行时下载的特定查看器、资产和CSS使用。

您可以使用随IS查看器提供的生产就绪型HTML页面，在弹出模式下使用视频查看器。 或者，您也可以在嵌入式模式下使用查看器，在该模式下，可使用记录的API将查看器集成到目标网页中。

配置查看器并设置其外观的任务与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器 — URL通用的命令引用](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与视频查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

视频查看器为视频播放提供了一组标准用户界面控件，如播放/暂停按钮、视频清理器视频时间气泡、播放时间/总时间指示器、音量控制、全屏按钮和隐藏式字幕切换。 所有这些控件都分组到位于查看器用户界面底部的控制栏中。

在触控设备上，音量控制在用户界面中处于隐藏状态，因为只有使用硬件按钮才能控制音量。

当查看器在弹出模式下运行时，用户界面中不提供全屏按钮。

激活视频章节后，可以快速导航视频的内容。 视频章节在视频清理器跟踪中以标记形式显示，并在鼠标滚动时或在触控系统上点按时，显示章节标题和相关描述。 用户可以通过选择章节标记或选择章节描述气泡来查找特定章节。

查看器支持在Windows设备上通过触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可完全通过键盘访问。

请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 使用视频查看器共享社交媒体工具 {#section-907d316fe1da4b87abb9775f02464704}

视频查看器支持社交媒体共享工具。 用户界面中的按钮可用作单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏包含支持的每种类型共享渠道的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个包含相应数据输入表单的模式对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，在激活共享工具后，视频播放会自动暂停。

由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时，网页会提供一个链接，当选定该链接时，该链接会在单独的浏览器窗口中打开查看器。 在其他情况下，需要将查看器直接嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 通常，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频会自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户可以始终返回到该视频并继续播放。 唯一例外是，在Android™ 4.x设备上的Chrome浏览器中，这项规则可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向发生更改时进行调整。

此模式是移动设备最常使用的模式。 网页使用 `window.open()` JavaScript调用，已正确配置 `A` HTML元素，或任何其他合适的方法。

建议您使用现成的HTML页面进行弹出操作模式。 它名为 [!DNL VideoViewer.html] 它位于 [!DNL html5/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占据网页的一部分房地产。

主要用例包括面向台式机或平板电脑设备的网页，以及响应式设计页面，这些页面可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器的大小变化 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式与网页大小容器的方式有所不同 `DIV`. 如果网页仅设置容器的宽度 `DIV`，查看器会根据所使用资产的宽高比自动选择其高度，而不限制其高度。 此方法可确保资产完美地适合视图，而不会在侧边添加任何内边距。 对于使用响应式设计布局框架(如Bootstrap或基础)的网页，此用例最为常见。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口的大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML头中添加脚本标记。 在使用查看器API之前，请确保在 [!DNL FlyoutViewer.js]. 的 [!DNL FlyoutViewer.js] 文件位于 [!DNL html5/js/] 标准IS — 查看器部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在其中一个Adobe Dynamic Media Classic服务器上并且来自同一域，则可以使用相对路径。 否则，您将指定一个安装IS-Viewers的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
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

   确保全屏功能在Internet Explorer中正常运行。 检查以确保DOM中没有其他元素的堆叠顺序比占位符DIV高。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 设置查看器大小

   您可以通过声明查看器的静态大小 `.s7videoviewer` 以绝对单位表示的顶级CSS类，或使用修饰符 `stagesize`.

   您可以将大小调整直接放在CSSHTML页面上，或放在自定义查看器CSS文件中。 它稍后会被分配到Dynamic Media Classic中的查看器预设记录，或使用样式命令显式传递。

   请参阅 [自定义视频查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 有关使用CSS为查看器设置样式的更多信息。

   以下示例用于在HTML页面中定义静态查看器大小：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以设置 `stagesize` 修改量(在Dynamic Media Classic的查看器预设记录中)，或使用查看器初始化代码(通过 `params` 收藏集。 或者，作为API调用（如命令引用部分中所述），如下所示：

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   建议使用基于CSS的方法，该方法将在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.VideoViewer` 类，将所有配置信息传递给其构造函数并调用 `init()` 方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有 `containerId` 包含查看器容器ID和嵌套名称的字段 `params` 具有查看器支持的配置参数的JSON对象。 在这种情况下， `params` 对象必须至少将图像服务URL作为 `serverUrl` 属性，作为 `videoserverurl` 资产，初始资产则作为 `asset` 参数。 通过基于JSON的初始化API，您只需一行代码即可创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大兼容，请调用 `init()` 方法 `BODY` 标记，或在主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用 `display:none` 样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此操作时，查看器加载会自动恢复。

   以下示例用于创建查看器实例、向构造函数传递最小必需配置选项以及调用 `init()` 方法。 此示例假定 `videoViewer` 是查看器实例， `s7viewer` 是占位符的名称 `DIV`, [!DNL http://s7d1.scene7.com/is/image/] 是图像提供URL， [!DNL http://s7d1.scene7.com/is/content/] 是视频服务器URL， [!DNL Scene7SharedAssets/Glacier_Climber_MP4] 是资产。

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   以下代码是嵌入具有固定大小的视频查看器的普通网页的完整示例：

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**具有无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指示查看器容器的运行时大小 `DIV`. 就本例而言，假定网页允许查看者的容器 `DIV` 可获取Web浏览器窗口大小的40%，从而使其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面类似于固定大小嵌入；唯一的区别在于您无需明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同。 添加容器 `DIV` 至现有“持有人” `DIV`. 以下代码是一个完整的示例。 您可以查看在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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

其余嵌入步骤与具有无限制高度的响应式设计嵌入步骤相同。 结果示例如下：

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
