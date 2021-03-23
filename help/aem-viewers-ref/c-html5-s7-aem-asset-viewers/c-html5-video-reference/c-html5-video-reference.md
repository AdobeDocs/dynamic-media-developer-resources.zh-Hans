---
description: 视频查看器是一个视频播放器，可播放以H.264格式编码的流式和渐进式视频。 它是从Dynamic Media Classic或AEM Dynamic Media提供的。
keywords: 响应
solution: Experience Manager
title: 视频
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# 视频{#video}

视频查看器是一个视频播放器，可播放以H.264格式编码的流式和渐进式视频。 它是从Dynamic Media Classic或AEM Dynamic Media提供的。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

同时支持单个视频和自适应视频集。 此外，查看器还支持使用外部位置上托管的渐进式视频和HLS流。 它设计为可在支持HTML5视频的桌面和移动Web浏览器上使用。 此查看器还支持视频内容顶部显示的可选隐藏式字幕、视频章节导航和社交媒体共享工具。

当基础系统支持视频查看器时，视频查看器在其默认配置中使用HLS格式的HTML5流视频回放。 在不支持HTML5流的系统上，查看器回退到HTML5渐进式视频投放。

查看器类型506。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用视频查看器{#section-f21ac23d3f6449ad9765588d69584772}

视频查看器代表一个主JavaScript文件和一组帮助文件 — 单个JavaScript包含在该特定查看器、资源和查看器在运行时下载的CSS使用的所有查看器SDK组件中。

您可以使用随IS-Viewers提供的生产就绪型HTML页面，在弹出模式下使用视频查看器。 或者，您可以在嵌入式模式下使用查看器，在嵌入式模式下，使用文档化的API将查看器集成到目标网页中。

配置查看器和设置查看器外观的任务与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅所有查看器的通用命令参考 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看器通用的通用命令参考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[[

## 与视频查看器{#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}交互

Video Viewer为视频播放提供了一套标准用户界面控件，如播放/暂停按钮、视频浏览器视频时间泡、播放时间/总时间指示器、音量控制、全屏按钮和隐藏字幕切换。 所有这些控件都分组到查看器用户界面底部的控件栏中。

在触控设备上，音量控制在用户界面中是隐藏的，因为只有使用硬件按钮才能控制音量。

查看器在弹出模式下操作时，用户界面中不提供全屏按钮。

激活视频分页时，可以快速导航视频内容。 视频章节在视频浏览器轨道中显示为标记，并在鼠标悬停或在触控系统上点击一次时显示章节标题和相关说明。 用户可以通过单击章节标记或点击章节描述气泡来查找特定章节。

查看器支持在Windows设备上使用触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器完全可通过键盘访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用Video Viewer {#section-907d316fe1da4b87abb9775f02464704}的社交媒体共享工具

视频查看器支持社交媒体共享工具。用户界面中的单个按钮可用，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏包含支持的每种类型的共享渠道的图标，如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器将显示一个带有相应数据输入表单的模态对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频播放会自动暂停。

由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入视频查看器{#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看器行为有不同的需求。 有时，网页会提供链接，单击该链接后，查看器将在单独的浏览器窗口中打开。 在其他情况下，必须将查看器直接嵌入到托管页面。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同的内容，或针对不同的浏览器窗口大小显示不同的内容。 为满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 在大多数情况下，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，会自动暂停第一个视频。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回并继续播放。 此规则的唯一例外是Android 4.x设备上的Chrome浏览器，它可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式是移动设备最常见的模式。 该网页使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议您使用现成的HTML页面进行弹出操作模式。 它名为[!DNL VideoViewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以通过应用自定义CSS实现可视自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器将添加到现有网页，该网页可能已包含一些与查看器无关的客户内容。 查看器通常仅占据网页的一部分空间。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入假定查看器可能需要在运行时调整大小以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式中，查看器的行为方式因网页调整其容器`DIV`的方式而异。 如果网页仅设置容器的宽度`DIV`，而保持高度不受限，则查看器会根据所使用资产的宽高比自动选择其高度。 此方法可确保资产完美地适合视图，而不会在两侧填充任何内边。 此用例是使用响应式设计布局框架(如Bootstrap、Foundation等)的网页中最常见的用例。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个不错的示例是将查看器嵌入到模式叠加中，其中的叠加会根据Web浏览器窗口的大小进行调整。

**固定大小嵌入**

可通过执行以下操作，将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要在HTML头中添加脚本标签。 在使用查看器API之前，请确保包含[!DNL FlyoutViewer.js]。 [!DNL FlyoutViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在某台Adobe Dynamic Media Classic服务器上，并从同一域提供，则可以使用相对路径。 否则，您将指定一个指向安装了IS-Viewer的Adobe Dynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能由查看器的逻辑在运行时下载。 特别是，不要直接引用由查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是，`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生变化。 Adobe不会将旧版次查看器`includes`保留在服务器上。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时破坏查看器功能。

1. 定义容器DIV。

   向希望查看器显示的页面添加空DIV元素。 DIV元素必须定义其ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是定位元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   确保全屏功能在Internet Explorer中正常工作。 检查以确保DOM中没有其他元素的堆叠顺序高于占位符DIV。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 设置查看器大小

   您可以通过以下两种方式设置查看器的静态大小：以绝对单位为`.s7videoviewer`顶级CSS类声明查看器，或使用修饰符`stagesize`。

   CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配到Dynamic Media Classic中的查看器预设记录，或使用样式命令显式传递。

   有关使用CSS设置查看器样式的详细信息，请参阅[自定义视频查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)。

   以下是在HTML页面中定义静态查看器大小的示例：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic的查看器预设记录中设置`stagesize`修饰符，或将其显式传递给带有`params`集合的查看器初始化代码，或作为命令参考部分中所述的API调用进行传递，如下所示：

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   建议使用基于CSS的方法，并在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建`s7viewers.VideoViewer`类的实例，将所有配置信息传递给它的构造函数，并对查看器实例调用`init()`方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称以及查看器支持的配置参数嵌套的`params` JSON对象。 在这种情况下，`params`对象必须至少具有作为`serverUrl`属性传递的图像服务URL、作为`videoserverurl`属性传递的视频服务器URL以及作为`asset`参数传递的初始资产。 基于JSON的初始化API允许您使用单行代码创建和开始查看器。

   务必将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会将构建DOM延迟到网页结束。 要获得最大兼容性，请在结束`BODY`标签之前或在正文`onload()`事件上调用`init()`方法。

   同时，容器元素还不一定是网页布局的一部分。 例如，可能会使用分配给它的`display:none`样式将其隐藏。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素返回到布局时为止。 发生这种情况时，查看器加载会自动恢复。

   以下是创建查看器实例、将最小必要配置选项传递给构造函数并调用`init()`方法的示例。 此示例假定`videoViewer`为查看器实例，`s7viewer`为占位符`DIV`的名称，[!DNL http://s7d1.scene7.com/is/image/]为图像服务URL，[!DNL http://s7d1.scene7.com/is/content/]为视频服务器URL，[!DNL Scene7SharedAssets/Glacier_Climber_MP4]为资产。

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

   以下代码是嵌入具有固定大小的视频查看器的次要网页的完整示例：

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

**无限制高度的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，指示查看器容器的运行时大小`DIV`。 为本示例之目的，假定网页允许查看器的容器`DIV`采用Web浏览器窗口大小的40%，同时保持其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小的嵌入非常相似；唯一的区别是您无需显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述步骤与固定大小嵌入相同。 将容器`DIV`添加到现有的&quot; holder&quot; `DIV`。 以下代码是一个完整的示例。 您可以查看调整浏览器大小时查看器大小的更改方式，以及查看器长宽比与资产的匹配方式。

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

以下示例页面演示了无限制高度的响应式设计嵌入在现实生活中的更多用途：

[实时演示](https://landing.adobe.com/zh-Hans/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**定义了宽度和高度的响应式设计嵌入**

在定义了宽度和高度的响应式设计嵌入时，网页的样式有所不同；它为“holder”`DIV`提供两种大小，并将其居中在浏览器窗口中。 此外，网页会将`HTML`和`BODY`元素的大小设置为100%:

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

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API，构造函数不采用任何参数，而配置参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

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

