---
description: 配置属性直接定义为响应式图像库管理的IMG元素上的属性。 每个图像都可以有其自己的一组属性。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

配置属性直接定义为响应式图像库管理的IMG元素上的属性。 每个图像都可以有其自己的一组属性。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

可选。

图像提供所提供图像的URL。 如果URL不存在，则库会使用`src`属性中设置的值作为回退。 此属性用于响应式图像库从不同位置管理的初始图像和动态图像。

**示例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果设置了`data-src`，则`src`是可选的，并且可以包含要添加的任何URL。 例如，它可以包含一个URL，指向库所用的相同基于图像服务的图像。 或者，它可以包含GIF占位符，甚至可以包含数据URI，以避免启动时出现额外的服务器往返。

如果未设置`data-src`，则`src`是必选项，并且必须包含图像服务所提供图像的URL。

**示例**

为`src`属性使用数据URI，为`data-src`属性使用图像服务URL:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 数据断点 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗号分隔的断点列表，其后可选择附加一个冒号(`:`)和“图像提供”命令或“图像预设”。 每个断点是在逻辑CSS像素中定义的图像宽度值。 库会使用列表中值最大的值加载图像，并在客户端上缩小图像，以匹配运行时CSS图像宽度。 （如果您在高密度屏幕上工作，则从服务器加载的图像呈现表示断点值乘以设备的像素比率。）

对于列表中的任何断点，可以定义一个或多个图像提供命令或图像预设名称。 此类额外参数仅在此特定断点当前处于活动状态时才应用于图像。

除了那些影响响应图像大小的视图命令（如`wid=`、`hei=`或`scl=`）之外，您可以使用任何受支持的图像服务命令。 图像预设也存在同样的限制：与响应式图像库一起使用的图像预设不得包含此类命令。

多个图像提供命令或图像预设名称之间以“ `&`”字符分隔。 如果图像提供命令的值中包含逗号，则此类逗号将替换为`%2C`。 图像预设名称用美元符号括起来(`$`)。

**示例**

**仅使用断点**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用图像提供命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用图像预设**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用图像预设和图像提供命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 数据模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4及更高版本以及Dynamic Media查看器5.9及更高版本中提供了以下两种智能裁剪模式：

* **手动**  — 在图像元素的属性中定义用户定义的断点和相应的图像服务命令。
* **智能裁剪**  — 计算的智能裁剪呈现版本会自动从投放服务器中进行检索。使用图像元素的运行时大小选择最佳演绎版。

要使用智能裁剪模式，请将`data-mode`属性设置为`smart crop`。

**示例**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

当断点发生更改时，关联的图像元素在运行时调度`s7responsiveViewer`事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
