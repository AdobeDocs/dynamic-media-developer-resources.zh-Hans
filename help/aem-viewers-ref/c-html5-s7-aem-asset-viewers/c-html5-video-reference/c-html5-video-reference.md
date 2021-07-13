---
description: 视频查看器是一个视频播放器，可播放以H.264格式编码的流视频和渐进式视频。 它从Dynamic Media Classic或AEM Dynamic Media提供。
keywords: 响应式
solution: Experience Manager
title: 视频
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 0%

---

# 视频{#video}

视频查看器是一个视频播放器，可播放以H.264格式编码的流视频和渐进式视频。 它从Dynamic Media Classic或AEM Dynamic Media提供。

请参阅[系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)。

同时支持单个视频集和自适应视频集。 此外，查看器还支持使用在外部位置托管的渐进式视频流和HLS流。 它可同时在支持HTML5视频的桌面和移动Web浏览器上使用。 此查看器还支持视频内容、视频章节导航和社交媒体共享工具顶部显示的可选隐藏式字幕。

当基础系统支持视频查看器时，视频查看器在其默认配置中使用HLS格式的HTML5流视频播放。 在不支持HTML5流播放的系统上，查看器会返回到HTML5渐进式视频交付。

查看器类型506。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## 使用视频查看器 {#section-f21ac23d3f6449ad9765588d69584772}

视频查看器表示一个主JavaScript文件和一组帮助程序文件 — 单个JavaScript包含的查看器SDK组件由该查看器在运行时下载的该特定查看器、资产和CSS使用。

您可以使用随IS-Viewers提供的生产就绪HTML页面，在弹出模式下使用视频查看器。 或者，您也可以在嵌入式模式下使用查看器，在该模式下，可使用记录的API将查看器集成到目标网页中。

配置查看器并设置其外观的任务与其他查看器类似。 所有外观设置都通过自定义CSS实现。

请参阅所有查看器的通用命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[

## 与视频查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

视频查看器为视频播放提供了一组标准用户界面控件，如播放/暂停按钮、视频清理器视频时间气泡、播放时间/总时间指示器、音量控制、全屏按钮和隐藏式字幕切换。 所有这些控件都分组到位于查看器用户界面底部的控制栏中。

在触控设备上，音量控制在用户界面中处于隐藏状态，因为只有使用硬件按钮才能控制音量。

当查看器在弹出模式下运行时，用户界面中不提供全屏按钮。

激活视频章节后，可以快速导航视频的内容。 视频章节在视频扫描器跟踪中显示为标记，并在鼠标悬停或在触控系统上单击鼠标时显示章节标题和相关描述。 用户可以通过单击章节标记或点按章节描述气泡来查找特定章节。

查看器支持在Windows设备上通过触摸屏和鼠标进行触摸输入和鼠标输入。 但是，此支持仅限于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可完全通过键盘访问。

请参阅[键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)。

## 使用视频查看器共享社交媒体工具 {#section-907d316fe1da4b87abb9775f02464704}

视频查看器支持社交媒体共享工具。这些工具在用户界面中以单个按钮的形式提供，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏包含支持的每种类型共享渠道的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个包含相应数据输入表单的模式对话框。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，在激活共享工具后，视频播放会自动暂停。

由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同网页对查看者行为的需求不同。 有时，网页会提供一个链接，单击该链接后，查看者便会在单独的浏览器窗口中打开。 在其他情况下，需要将查看器直接嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同设备上显示不同，或针对不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 在大多数情况下，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频会自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户可以始终返回到该视频并继续播放。 唯一例外是，在Android 4.x设备上的Chrome浏览器中，这项规则可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器在单独的Web浏览器窗口或选项卡中打开。 它会占用整个浏览器窗口区域，并在浏览器大小调整或设备方向发生更改时进行调整。

此模式是移动设备最常使用的模式。 网页会使用`window.open()` JavaScript调用、正确配置的`A` HTML元素或任何其他合适的方法加载查看器。

建议使用现成的HTML页面进行弹出操作模式。 它名为[!DNL VideoViewer.html]，位于标准IS-Viewers部署的[!DNL html5/]子文件夹下：

[!DNL <s7viewers_root>/html5/VideoViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器会添加到现有网页，该网页可能已经包含一些与查看器无关的客户内容。 查看者通常只占据网页的一部分房地产。

主要用例是面向台式机或平板电脑设备的网页，还有响应式设计页面，可根据设备类型自动调整布局。

当查看器在初始加载后不更改其大小时，会使用固定大小嵌入。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入假定查看器可能需要在运行时调整大小，以响应其容器`DIV`的大小变化。 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式与网页大小容器`DIV`的方式不同。 如果网页仅设置容器的宽度`DIV`，并且不限制其高度，则查看器会根据所使用资产的宽高比自动选择其高度。 此方法可确保资产完美地适合视图，而不会在侧边添加任何内边距。 对于使用响应式设计布局框架(如Bootstrap、基础等)的网页，此用例最为常见。

否则，如果网页同时设置查看器容器`DIV`的宽度和高度，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中的叠加根据Web浏览器窗口的大小来调整大小。

**固定大小嵌入**

可通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器`DIV`。
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器要求您在HTML标头中添加脚本标记。 在使用查看器API之前，请确保包含[!DNL FlyoutViewer.js]。 [!DNL FlyoutViewer.js]文件位于标准IS-Viewers部署的[!DNL html5/js/]子文件夹下：

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

如果查看器部署在某个Adobe的Dynamic Media Classic服务器上，并且从同一域提供该查看器，则可以使用相对路径。 否则，您将指定一个安装IS-Viewer的AdobeDynamic Media Classic服务器的完整路径。

相对路径如下所示：

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>您只应在页面上引用主查看器JavaScript `include`文件。 您不应在网页代码中引用任何其他JavaScript文件，这些文件可能会在运行时由查看器的逻辑下载。 特别是，切勿直接引用查看器从`/s7viewers`上下文路径加载的HTML5 SDK `Utils.js`库（所谓的统一SDK `include`）。 原因是`Utils.js`或类似的运行时查看器库的位置完全由查看器的逻辑管理，并且查看器版本之间的位置发生更改。 Adobe不会在服务器上保留旧版次查看器`includes`。
>
>
>因此，在页面上直接引用查看器使用的任何辅助JavaScript `include`会在将来部署新产品版本时中断查看器功能。

1. 定义容器DIV。

   在希望查看器显示的页面中添加空DIV元素。 必须定义DIV元素的ID，因为此ID稍后会传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是放置元素，这意味着`position` CSS属性设置为`relative`或`absolute`。

   确保全屏功能在Internet Explorer中正常运行。 检查以确保DOM中没有其他元素的堆叠顺序比占位符DIV高。

   以下是定义的占位符DIV元素的示例：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 设置查看器大小

   您可以通过以下两种方式设置查看器的静态大小：以绝对单位声明查看器的`.s7videoviewer`顶级CSS类，或使用修饰符`stagesize`。

   CSS中的大小调整可以直接放在HTML页面上，也可以放在自定义查看器CSS文件中，该文件稍后会分配给Dynamic Media Classic中的查看器预设记录，或使用样式命令显式传递。

   请参阅[自定义视频查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) ，以了解有关使用CSS为查看器设置样式的更多信息。

   以下示例用于在HTML页面中定义静态查看器大小：

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以在Dynamic Media Classic的查看器预设记录中设置`stagesize`修饰符，或通过查看器初始化代码（包含`params`集合）显式传递该修饰符，或者作为API调用（如命令引用部分所述）进行传递，如下所示：

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   建议使用基于CSS的方法，该方法将在此示例中使用。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个`s7viewers.VideoViewer`类的实例，将所有配置信息传递给其构造函数，并在查看器实例中调用`init()`方法。 配置信息作为JSON对象传递到构造函数。 此对象至少应具有`containerId`字段，该字段包含查看器容器ID的名称，以及嵌套的`params` JSON对象（具有查看器支持的配置参数）。 在这种情况下，`params`对象必须至少具有作为`serverUrl`属性传递的图像服务URL、作为`videoserverurl`属性传递的视频服务器URL，以及作为`asset`参数传递的初始资产。 通过基于JSON的初始化API，您只需一行代码即可创建和启动查看器。

   务必要将查看器容器添加到DOM，以便查看器代码可以通过其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结束。 为了实现最大的兼容性，请在结束`BODY`标记之前或在主体`onload()`事件上调用`init()`方法。

   同时，容器元素不一定只是网页布局的一部分。 例如，可以使用分配给它的`display:none`样式来隐藏它。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素引回布局时为止。 发生此情况时，查看器加载会自动恢复。

   以下示例用于创建查看器实例，将最小必需的配置选项传递给构造函数，并调用`init()`方法。 此示例假定`videoViewer`为查看器实例，`s7viewer`为占位符的名称`DIV`,[!DNL http://s7d1.scene7.com/is/image/]为图像服务URL，[!DNL http://s7d1.scene7.com/is/content/]为视频服务器URL，[!DNL Scene7SharedAssets/Glacier_Climber_MP4]为资产。

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

通过响应式设计嵌入，网页通常具有某种灵活的布局，指示查看器容器`DIV`的运行时大小。 就本例而言，假定网页允许查看器的容器`DIV`占用Web浏览器窗口大小的40%，并保持其高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与固定大小嵌入非常相似；唯一的区别在于您无需明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与固定大小嵌入的步骤相同。 将容器`DIV`添加到现有的“ holder” `DIV`中。 以下代码是一个完整的示例。 您可以查看在调整浏览器大小时查看器大小的变化情况，以及查看器长宽比与资产的匹配情况。

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

[替代演示位置](https://experienceleague.adobe.com/tools/vlist/vlist.html)

**定义宽度和高度的响应式设计嵌入**

在定义了宽度和高度的响应式设计嵌入时，网页的样式不同；它为“ holder” `DIV`提供两种大小，并将其放在浏览器窗口的中心。 此外，该网页还会将`HTML`和`BODY`元素的大小设置为100%:

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

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用该API时，构造函数不会获取任何参数，并且配置参数是使用具有单独JavaScript调用的`setContainerId()`、`setParam()`和`setAsset()` API方法指定的。

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
