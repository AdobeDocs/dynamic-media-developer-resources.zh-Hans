---
description: 配置属性直接在Responsive图像库管理的IMG元素上定义为属性。 每个图像可以有自己的一组属性。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

配置属性直接在Responsive图像库管理的IMG元素上定义为属性。 每个图像可以有自己的一组属性。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

可选.

“图像服务”提供的图像的URL。 如果URL不存在，则库将使用中设置的值 `src` 归因为回退。 此属性用于提供Responsive图像库从不同位置管理的初始图像和动态图像。

**示例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果 `data-src` 已设置， `src` 是可选的，并且可以包含要添加的任何网址。 例如，它可以包含指向库使用的相同基于图像服务的图像的URL。 或者，它可以包含GIF占位符甚至数据URI，以避免启动时额外的服务器来回访问。

如果 `data-src` 未设置， `src` 是必需的，必须包含图像服务所服务图像的URL。

**示例**

将数据URI用于 `src` 的属性和图像服务URL `data-src` 属性：

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 数据断点 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗号分隔的断点列表，并可以选择后跟冒号( `:`)，以及图像服务命令或图像预设。 每个断点是以逻辑CSS像素定义的图像宽度值。 库将加载列表中值最大的图像，并在客户端上缩小该图像以匹配运行时CSS图像宽度。 （如果您在高密度屏幕上工作，则从服务器加载的图像演绎版表示断点值乘以设备的像素比）。

对于列表中的任何断点，都可以定义一个或多个图像提供命令或图像预设名称。 此类额外参数仅适用于该特定断点当前处于活动状态时的图像。

您可以使用任何受支持的图像服务命令，但会影响响应图像大小的视图命令除外，例如 `wid=`， `hei=`，或 `scl=`. 相同的限制也适用于图像预设：与Responsive图像库一起使用的图像预设不得包含此类命令。

多个图像服务命令或图像预设名称之间使用&quot; `&`”字符。 如果图像服务命令的值中包含逗号，则此类逗号会被替换为 `%2C`. 图像预设名称将用美元符号( `$`)。

**示例**

**仅使用断点**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用图像服务命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用图像预设**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用图像预设和图像服务命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 数据模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4及更高版本和Dynamic Media Viewer 5.9及更高版本中提供了以下两种智能裁切模式：

* **手动**  — 用户定义的断点和相应的图像服务命令在图像元素的属性中定义。
* **智能裁剪**  — 自动从投放服务器检索计算智能裁剪演绎版。 使用图像元素的运行时大小选择最佳演绎版。

要使用智能裁剪模式，请设置 `data-mode` 属性至 `smart crop`.

**示例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

关联的图像元素调度 `s7responsiveViewer` 运行时断点更改时的事件。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
