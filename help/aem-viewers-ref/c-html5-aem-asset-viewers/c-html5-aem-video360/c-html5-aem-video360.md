---
title: Video360
description: HTML5 Video360 Viewer是一款360度视频播放器，可播放从Dynamic Media Classic或Adobe Experience Manager、Dynamic Media交付的H.264格式的流视频和渐进式360视频。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2568'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360 Viewer是一款360度视频播放器，可播放从Dynamic Media Classic或Adobe Experience Manager、Dynamic Media交付的H.264格式的流视频和渐进式360视频。

360度视频，也称为沉浸式视频或球形视频，是同时录制每个方向的视图的视频录像，使用全方位相机或相机集合拍摄。 支持单个视频和自适应视频集。 查看器还支持使用托管在外部位置的渐进式视频流和HLS流。

360视频的推荐长宽比为2:1。 不支持空间声音。 查看器仅适用于360视频；尝试播放非360视频会导致视频播放失真。

查看器可在支持HTML5视频的桌面和移动Web浏览器上使用。 查看器支持可选的社交共享工具。

只要基础系统支持，Video360查看器就会在其默认配置中使用HLS格式的HTML5流视频播放。 在不支持HTML5流式传输的系统上，查看器回退到HTML5渐进式视频交付。

查看器类型为517。

## 演示URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

请参阅 [系统要求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 使用Video360查看器 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer表示一个主JavaScript文件和一组帮助程序文件(单个JavaScript包含此查看器使用的所有HTML5 Viewer SDK组件、资源、CSS)，这些文件由查看器在运行时下载。

HTML5 Video360查看器既可以使用随IS-Viewers提供的生产就绪HTML页的弹出模式，也可以使用嵌入模式（使用文档记录的API将其集成到目标网页中）。

配置和外观设计类似于本指南中描述的其他查看器的配置和外观。 所有外观设计都是通过自定义(CSS)层叠样式表实现的。

请参阅 [所有查看器通用的命令引用 — 配置属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有查看器通用的命令引用 — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360视频内容所需的编码设置比标准的非360视频更高。 换句话说，360内容必须比非360视频具有更高的分辨率，才能获得相同的可感知质量。 建议您考虑为360视频设置以下自适应视频预设：

* 720p， 2500 kbps
* 1080p， 5000 kbps
* 1440p， 6600 kbps

但请注意，为使用此类高质量设置编码的视频提供服务，需要在最终用户设备上使用高带宽连接。

## 与Video360查看器交互 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360查看器提供一组用于视频播放的标准用户界面控件，如播放/暂停按钮、视频洗刷视频时间气泡、播放时间/总时间指示器、音量控件和全屏按钮。 所有这些控件都分组到查看器用户界面底部的控件栏中。

在触控设备上，音量控制对用户界面是隐藏的，因为只能使用设备的硬件按钮来控制音量。

当查看器以弹出模式运行时，全屏按钮在用户界面中不可用。

查看器还支持各种社交媒体共享工具。 它们可用作用户界面中的单个按钮，当用户单击或点按时，该按钮将扩展为共享工具栏。 共享工具栏中包含有关支持的每种共享渠道类型的图标，例如Facebook、Twitter、电子邮件共享、嵌入代码共享和链接共享。 激活电子邮件共享、嵌入共享或链接共享工具后，查看器会显示一个模式对话框，其中包含相应的数据输入表单。 调用Facebook或Twitter时，查看器会将用户从社交媒体服务重定向到标准共享对话框。 此外，当共享工具激活时，视频播放会自动暂停。 由于Web浏览器安全限制，共享工具在全屏模式下不可用。

查看器支持以下内容的360视频播放：

* VR耳机(如Oculus Go和Oculus Rift)
* VR HMD（头戴式显示器）安装(如Google Cardboard)
* 非VR支持的设备（如桌面浏览器、平板电脑和手机未连接到VR HMD安装架）

无需额外配置即可在VR头戴式耳机上查看360视频内容。 查看器会自动检测VR头戴式耳机是否存在，并在视频内容上方显示“VR”按钮。 激活此“VR”按钮会将视频渲染切换到VR模式。 查看器仅在支持WebVR的浏览器中支持VR渲染。

要使用VR HMD，请安装 `Video360Player.vrrender` 修饰符必须设置为 `1` 在查看器的配置中，强制进行立体渲染。

在VR头戴式耳机和VR HMD安装上，视点改变响应于头戴式耳机的运动而发生，而不是在VR模式下提供其它回放控制。

在非支持VR的设备上观看360视频时，最终用户可以使用鼠标、触摸或键盘来控制视频播放和视点。

该查看器支持在带有触摸屏和鼠标的Windows设备上输入触摸和鼠标，但仅支持Chrome、Internet Explorer 11和Edge Web浏览器。

查看器完全可使用键盘。 请参阅 [键盘辅助功能和导航](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 嵌入Video360查看器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的网页对查看者的行为具有不同的需求。 有时，网页会提供一个链接，选中该链接后，查看器将在单独的浏览器窗口中打开。 在其他情况下，需要直接将查看器嵌入到托管页面上。 在后一种情况下，网页可能具有静态页面布局，或者使用响应式设计，该设计在不同的设备上或对于不同的浏览器窗口大小显示不同。 为了满足这些需求，查看器支持三种主要操作模式：弹出窗口、固定大小嵌入和响应式设计嵌入。

平板电脑和移动设备支持在同一页面上嵌入多个视频。 通常，一次只能播放一个视频。 当用户开始播放一个视频，然后尝试播放另一个视频时，第一个视频自动暂停。 自动暂停的视频会记住其当前播放时间，因此用户始终可以返回并继续播放。 唯一的例外是在Android™ 4.x设备上的Chrome浏览器中，该浏览器可以并行播放视频。

**关于弹出模式**

在弹出模式下，查看器将在单独的Web浏览器窗口或选项卡中打开。 它采用整个浏览器窗口区域，并在浏览器大小调整或设备方向更改时进行调整。

此模式最适用于移动设备。 网页使用以下方式加载查看器 `window.open()` JavaScript调用，正确配置 `A` HTML元素或任何其他适当的方法。

建议您为弹出操作模式使用现成的HTML页面。 此函数名为 [!DNL Video360Viewer.html] 它位于 [!DNL html5/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

您可以通过应用自定义CSS来实现可视化自定义。

以下是在新窗口中打开查看器的HTML代码示例：

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**关于固定大小嵌入模式和响应式设计嵌入模式**

在嵌入模式下，查看器将添加到现有网页，这些网页可能已有一些与查看器无关的客户内容。 查看者通常只占用网页不动产的一部分。

主要用例是面向台式机或平板电脑设备的网页，以及根据设备类型自动调整布局的响应式设计页面。

当查看器在初始加载后未更改其大小时，使用固定大小嵌入。 对于具有静态布局的网页，此方法为最佳选择。

响应式设计嵌入假定查看器必须在运行时调整大小以响应其容器的大小更改 `DIV`. 最常见的用例是将查看器添加到使用灵活页面布局的网页。

在响应式设计嵌入模式下，查看器的行为方式有所不同，具体取决于网页确定其容器大小的方式 `DIV`. 如果网页仅设置容器的宽度 `DIV`如果不限制高度，查看器将根据所用资源的纵横比自动选择高度。 此功能可确保资产完全适合视图，不会出现任何边距。 此用例最常用于使用响应式Web设计布局框架(如Bootstrap和Foundation)的网页。

否则，如果网页同时设置了查看器容器的宽度和高度 `DIV`，则查看器仅填充该区域，并遵循网页布局提供的大小。 一个很好的示例是将查看器嵌入到模式叠加中，其中叠加根据Web浏览器窗口大小调整大小。

**固定大小嵌入**

通过执行以下操作将查看器添加到网页：

1. 将查看器JavaScript文件添加到网页。
1. 定义容器 `DIV`.
1. 设置查看器大小。
1. 创建和初始化查看器。

1. 将查看器JavaScript文件添加到网页。

   创建查看器需要您在HTML头中添加脚本标记。 在使用查看器API之前，请确保包含 [!DNL Video360Viewer.js]. 此 [!DNL Video360Viewer.js] 文件位于 [!DNL html5/js/] 标准IS-Viewers部署的子文件夹：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

如果查看器部署在某个Adobe Dynamic Media Classic服务器上，并且来自同一域，则可以使用相对路径。 否则，您需要为其中一台安装了IS-Viewers的Adobe Dynamic Media Classic服务器指定完整路径。

相对路径如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>仅引用主查看器JavaScript `include` 文件上传到您的页面上。 请勿在网页代码中引用任何其他JavaScript文件，这些文件可能会在运行时由查看器的逻辑下载。 特别是，请勿直接引用HTML5 SDK `Utils.js` 由查看器加载的库，从 `/s7viewers` 上下文路径（所谓的整合SDK） `include`)。 原因在于 `Utils.js` 或者类似的运行时查看器库完全由查看器的逻辑管理，并且查看器版本之间的位置会发生变化。 Adobe不保留辅助查看器的旧版本 `includes` 在服务器上。
>
>
>因此，将直接引用放置到任何辅助JavaScript `include` 将来在部署新产品版本时，页面上查看器使用的功能会中断查看器。

1. 定义容器 `DIV`.

   添加空 `DIV` 元素到您希望查看器显示的页面。 此 `DIV` 元素必须定义其ID，因为此ID稍后传递给查看器API。 DIV的大小通过CSS指定。

   占位符 `DIV` 是一个定位元素，这意味着 `position` CSS属性设置为 `relative` 或 `absolute`.

   要使全屏功能在Internet Explorer中正常运行，请确保DOM中没有其他元素的栈叠顺序高于占位符 `DIV`.

   以下是定义的占位符示例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. 设置查看器大小

   您可以通过声明查看器的静态大小来为其设置静态大小。 `.s7video360viewer` 顶级CSS类（以绝对单位表示），或者使用 `stagesize` 修饰符。

   您可以将CSS的大小直接放在“HTML”页面或自定义查看器CSS文件中，该文件稍后将分配给Adobe Experience Manager Assets中的查看器预设记录（按需），或者使用进行明确传递 `style` 命令。

   请参阅 [自定义Video360查看器](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 有关使用CSS为查看器设置样式的更多信息。

   以下是在“HTML”页中定义静态查看器大小的示例：

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以设置 `stagesize` AEM Assets中的查看器预设记录中的修饰符 — 按需。 或者，您可以使用查看器初始化代码显式传递它 `params` 收藏集，或作为API调用，如命令引用部分中所述，如下所示：

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   此示例中建议并使用基于CSS的方法。

1. 创建和初始化查看器。

   完成上述步骤后，您将创建一个实例 `s7viewers.Video360Viewer` 类，将所有配置信息传递到其构造函数，并调用 `init()` 方法。 配置信息作为JSON对象传递给构造函数。 此对象至少应具有 `containerId` 保存查看器容器ID名称并嵌套的字段 `params` 包含查看器支持的配置参数的JSON对象。

   在本例中， `params` 对象必须至少将图像服务URL传递为 `serverUrl` 资产，而初始资产为 `asset` 参数。 基于JSON的初始化API允许您创建并启动查看器，只需一行代码，视频服务器URL作为 `videoserverurl` 资产，初始资产为 `asset` 参数，交互式数据为 `interactivedata` 属性。 基于JSON的初始化API允许您通过一行代码创建和启动查看器。

   必须将查看器容器添加到DOM，以便查看器代码可以按其ID查找容器元素。 某些浏览器会延迟构建DOM，直到网页结尾。 要获得最大的兼容性，请调用 `init()` 紧靠结束位置之前的方法 `BODY` 标记上，或主体上 `onload()` 事件。

   同时，容器元素还不一定是网页布局的一部分。 例如，可以使用隐藏该内容 `display:none` 为其分配的样式。 在这种情况下，查看器会延迟其初始化过程，直到网页将容器元素带回布局为止。 发生这种情况时，查看器加载会自动恢复。

   以下示例用于创建查看器实例，将所需的最少配置选项传递给构造函数并调用 `init()` 方法。 此示例假设以下内容：

   * 查看器实例为 `video360Viewer`.
   * 占位符的名称 `DIV` 是 `s7viewer`.
   * 图像服务URL为 `https://s7d9.scene7.com/is/image`.
   * 视频服务器URL为 `https://s7d9.scene7.com/is/content`.
   * 资产是 `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   以下代码是嵌入Video360查看器且大小固定的普通网页的完整示例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的响应式设计嵌入**

通过响应式设计嵌入，网页通常具有某种灵活的布局，可指定查看器容器的运行时大小 `DIV`. 对于以下示例，假设网页允许查看器的容器 `DIV` 占用Web浏览器窗口大小的40%，高度不受限制。 网页HTML代码如下所示：

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

将查看器添加到此类页面与嵌入固定大小的步骤类似。 唯一的区别是，您不需要显式定义查看器大小。

1. 将查看器JavaScript文件添加到网页。
1. 定义容器DIV。
1. 创建和初始化查看器。

上述所有步骤与嵌入固定大小相同。 将容器DIV添加到现有 `"holder"` 目录 以下代码是一个完整的示例。 请注意当浏览器调整大小时查看器大小如何变化，以及查看器长宽比如何与资源匹配。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**定义宽度和高度的响应式嵌入**

如果有定义了宽度和高度的响应式嵌入，则网页样式会不同。 它提供两种大小到 `"holder"` 在浏览器窗口中进行DIV和居中。 此外，该网页还设置 `HTML` 和 `BODY` 元素为100%。

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

其余嵌入步骤与用于高度不受限制的响应式嵌入的步骤相同。 生成的示例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用基于Setter的API进行嵌入**

可以使用基于setter的API和no-args构造函数，而不是使用基于JSON的初始化。 使用此API构造函数不接受任何参数，并且配置参数是使用 `setContainerId()`， `setParam()`、和 `setAsset()` API方法具有单独的JavaScript调用。

以下示例说明了如何将固定大小嵌入与基于setter的API一起使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
