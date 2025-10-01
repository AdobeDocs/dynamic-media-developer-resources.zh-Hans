---
description: 配置属性直接在Responsive图像库管理的IMG元素上定义为属性。 每个图像可以有自己的一组属性。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: 3df884c468ea89cc55b2b8ce13af01bfad454545
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

配置属性直接在Responsive图像库管理的IMG元素上定义为属性。 每个图像可以有自己的一组属性。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

可选.

图像服务所提供图像的URL。 如果URL不存在，则库将使用`src`属性中设置的值作为回退。 此属性用于提供初始图像和Responsive图像库从不同位置管理的动态图像。
<!--
**Example** 

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```
-->

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果设置了`data-src`，则`src`是可选的，可以包含您要添加的任何URL。 例如，它可以包含一个URL，指向库使用的基于图像服务的相同图像。 或者，它可以包含GIF占位符甚至数据URI，以避免启动时额外的服务器来回访问。

如果未设置`data-src`，则`src`是必需的，并且必须包含图像服务所服务图像的URL。

<!--
**Example**

Using data URI for the `src` attribute and Image Serving URL for the `data-src` attribute:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```
-->

## 数据断点 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗号分隔的断点列表，可选择后跟冒号(`:`)，以及图像服务命令或图像预设。 每个断点是以逻辑CSS像素定义的一个图像宽度值。 库将加载列表中值最近的图像，并在客户端上缩小该值以匹配运行时CSS图像宽度。 （如果在高密度屏幕上工作，则从服务器加载的图像演绎版表示断点值乘以设备的像素比）。

对于列表中的任何断点，都可以定义一个或多个图像提供命令或图像预设名称。 此类额外参数仅适用于该特定断点当前处于活动状态时的图像。

您可以使用任何受支持的图像服务命令，但会影响响应图像大小的视图命令除外，如`wid=`、`hei=`或`scl=`。 同样的限制也适用于图像预设：与Responsive图像库一起使用的图像预设不得包含此类命令。

多个图像服务命令或图像预设名称使用“`&`”字符分隔。 如果图像服务命令的值中包含逗号，则此类逗号将替换为`%2C`。 图像预设名称用美元符号(`$`)括起来。

<!--
**Examples**

**Using breakpoints only**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Using Image Serving commands**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Using Image Presets**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Using Image Presets & Image Serving commands**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

-->

## 数据模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4及更高版本和Dynamic Media Viewer 5.9及更高版本中有以下两种智能裁切模式可用：

* **手动** — 用户定义的断点和相应的图像服务命令在图像元素的属性中定义。
* **智能裁切** — 将自动从投放服务器中检索计算智能裁切再现。 使用图像元素的运行时大小选择最佳演绎版。

要使用智能裁剪模式，请将`data-mode`属性设置为`smart crop`。

**示例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

当断点更改时，关联的图像元素在运行时调度`s7responsiveViewer`事件。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
