---
title: 智能裁剪视频查看器
description: 智能裁切视频查看器可播放以H.264格式编码的流视频和渐进视频，并增加了智能裁切支持。 它通过Dynamic Media Classic或Adobe Experience Manager与Dynamic Media一起提供。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2399'
ht-degree: 0%

---

# 智能裁剪视频{#smart-crop-video}

智能裁切视频查看器可播放以H.264格式编码的流视频和渐进视频，并增加了智能裁切支持。 它是从Dynamic Media Classic或通过Dynamic MediaExperience Manager提供的。

请参阅 [系统要求和先决条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

支持单个视频和自适应视频集。 此外，查看器支持使用托管在外部位置的渐进式视频和HLS流。 它设计为可在支持HTML5视频的桌面和移动Web浏览器上工作。 此查看器还支持在视频内容、视频章节导航和社交媒体共享工具顶部显示的可选隐藏式字幕。

只要基础系统支持，智能裁剪视频查看器就会在其默认配置中使用HLS格式的HTML5流式视频播放。 在不支持HTML5流式传输的系统上，查看器回退到HTML5渐进式视频交付。

查看器类型518。

## 演示URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## 使用智能裁剪视频查看器 {#section-f21ac23d3f6449ad9765588d69584772}

智能裁剪视频查看器表示一个主JavaScript文件和一组帮助程序文件 — 单个JavaScript包含此特定查看器、资源和查看器在运行时下载的所有Viewer SDK组件。

您可以使用随IS-Viewers提供的生产就绪型HTML页，在弹出模式下使用智能裁切视频查看器。 或者，您可以在嵌入模式下使用查看器，在该模式下，使用文档记录的API将其集成到目标网页中。

配置查看器和为其设置外观的任务与其他查看器的任务类似。 所有外观设计都是通过自定义CSS实现的。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 与智能裁剪视频查看器交互 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

智能裁剪视频查看器为视频播放提供一组标准用户界面控件，例如：

* 播放/暂停按钮。
* 视频洗刷视频时间气泡。
* 已播放时间/总时间指示器。
* 音量控制。
* 全屏按钮。
* 隐藏式字幕切换。

所有这些控件都分组到查看器用户界面底部的控件栏中。

在触控设备上，音量控制对用户界面是隐藏的，因为只能使用硬件按钮控制音量。

当查看器以弹出模式运行时，全屏按钮在用户界面中不可用。

在激活视频章节时，可以快速导航视频内容。 视频章节将作为标记显示在视频洗刷轨道中，并在鼠标滚动或点按触摸系统时显示章节标题和相关描述。 用户可以通过选择章节标记或选择章节描述气泡来查找特定章节。

该查看器支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标。 但是，此支持仅适用于Chrome、Internet Explorer 11和Edge Web浏览器。

此查看器可使用键盘完全访问。

请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 使用智能裁剪视频查看器的社交媒体共享工具 {#section-907d316fe1da4b87abb9775f02464704}

智能裁剪视频查看器支持社交媒体共享工具。 它们可用作用户界面中的单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。

共享工具栏中包含支持的各种共享渠道类型的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个模式对话框，其中包含相应的数据输入表单。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具被激活时，视频播放也会自动暂停。

由于Web浏览器安全限制，共享工具在全屏模式下不可用。

## 嵌入智能裁剪视频查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供一个链接，选中该链接后，查看器将在单独的浏览器窗口中打开。 在其他情况下，需要直接将查看器嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同的设备上或对于不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 通常，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回并继续播放。 唯一的例外是在Android™ 4.x设备上的Chrome浏览器中，该浏览器可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式最适用于移动设备。 网页使用以下方式加载查看器 `window.open()` JavaScript调用，正确配置 `A` HTML元素或任何其他适当的方法。

建议您为弹出操作模式使用现成的HTML页面。 此函数名为 [!DNL SmartCropVideoViewer.html] 它位于 [!DNL html5/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式嵌入模式**

在嵌入模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 此选项最适合具有静态页面布局的网页。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器的大小更改 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页确定其容器大小的方式 `DIV`. 如果网页仅设置容器的宽度 `DIV`如果不限制高度，查看器将根据所用资源的纵横比自动选择高度。 此方法可确保资产完全适合视图，而不会在两侧添加任何边距。 此用例最常见于使用响应式设计布局框架(如Bootstrap或基础)的网页。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口的大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要您在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含 [!DNL SmartCropVideoViewer.js]. 此 [!DNL SmartCropVideoViewer.js] 文件位于 [!DNL html5/js/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件上传到您的页面上。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能会在运行时由查看器的逻辑下载。 特别是，请勿直接引用HTML5 SDK `Utils.js` 由查看器加载的库，从 `/s7viewers` 上下文路径（所谓的整合SDK） `include`)。 原因在于 `Utils.js` 或者类似的运行时查看器库完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不保留辅助查看器的旧版本 `includes` 在服务器上。
>
>
>因此，将直接引用放置到任何辅助JavaScript `include` 将来在部署新产品版本时，页面上查看器使用的功能会中断查看器。

1. 定义容器DIV。

   向要显示查看器的页面添加一个空DIV元素。 DIV元素必须定义其ID，因为此ID稍后将传递到查看器API。 DIV的大小通过CSS指定。

   占位符DIV是一个定位元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   确保全屏功能在Internet Explorer中正常工作。 检查以确保DOM中没有其他元素的栈叠顺序高于占位符DIV。

   以下是定义的占位符DIV元素的示例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 设置查看器大小

   您可以通过声明查看器的静态大小来为其设置静态大小。 `.s7videoviewer` 顶级CSS类（以绝对单位表示），或者使用修饰符 `stagesize`.

   您可以在HTML页面或自定义查看器CSS文件中直接在CSS中放置大小。 之后，会将该配置文件分配给Dynamic Media Classic中的查看器预设记录，或者使用样式命令显式传递配置文件。

   请参阅 [自定义智能裁剪视频查看器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 有关使用CSS设置查看器样式的更多信息。

   以下是在HTML页中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以设置 `stagesize` 在Dynamic Media Classic中的查看器预设记录中进行修饰符，或通过查看器初始化代码将其显式传递 `params` 收藏集。 或者，作为API调用，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.SmartCropVideoViewer` 类，将所有配置信息传递到其构造函数，并调用 `init()` 方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有 `containerId` 保存查看器容器ID名称并嵌套的字段 `params` 包含查看器支持的配置参数的JSON对象。 在本例中， `params` 对象必须至少将图像服务URL传递为 `serverUrl` 属性，视频服务器URL传递为 `videoserverurl` 资产，而初始资产为 `asset` 参数。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大的兼容性，请调用 `init()` 紧靠结束位置之前的方法 `BODY` 标记上，或主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用隐藏该内容 `display:none` 为其分配的样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 执行此操作后，查看器加载将自动继续。

   以下示例用于创建查看器实例，将最低必要的配置选项传递给构造函数，并调用 `init()` 方法。 此示例假定 `smartCropVideoViewer` 是查看器实例， `s7viewer` 是占位符的名称 `DIV`， [!DNL http://s7d1.scene7.com/is/image/] 是图像服务URL， [!DNL http://s7d1.scene7.com/is/content/] 是视频服务器URL，并且 [!DNL html5automation/frisbee-AVS] 是资产。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   以下代码是一个简单网页的完整示例，该网页以固定大小嵌入了智能裁切视频查看器：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看者容器的运行时大小 `DIV`. 在本例中，假设网页允许查看器的容器 `DIV` 占用Web浏览器窗口大小的40%，高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与嵌入固定大小类似；唯一的区别是无需明确定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 添加容器 `DIV` 到现有“持有者” `DIV`. 以下代码是一个完整的示例。 您可以查看在调整浏览器大小时查看器大小的变化情况，以及查看器纵横比与资源的匹配情况。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下示例页面说明了如何更真实地使用高度不受限制的响应式设计嵌入：

[实时演示](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[备用演示位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定义宽度和高度的响应式设计嵌入**

如果有定义了宽度和高度的响应式设计嵌入，则网页样式将不同；它将两种大小都提供给“支架” `DIV` 并将其居中在浏览器窗口中。 此外，该网页还设置 `HTML` 和 `BODY` 元素至100%：

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

其余嵌入步骤与高度不受限制的响应式设计嵌入相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 在该API中，构造函数不接受任何参数，并且配置参数使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法具有单独的JavaScript调用。

以下示例说明了使用基于setter的API嵌入固定大小：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
