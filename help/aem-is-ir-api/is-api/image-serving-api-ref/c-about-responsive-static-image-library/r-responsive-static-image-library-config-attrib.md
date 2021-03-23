---
description: 配置属性直接定义为响应式图像库管理的IMG元素上的属性。 每个图像都可以有其自己的一组属性。
seo-description: 配置属性直接定义为响应式图像库管理的IMG元素上的属性。 每个图像都可以有其自己的一组属性。
seo-title: 命令参考 — 配置属性
solution: Experience Manager
title: 命令参考 — 配置属性
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# 命令引用 — 配置属性{#command-reference-configuration-attributes}

配置属性直接定义为响应式图像库管理的IMG元素上的属性。 每个图像都可以有其自己的一组属性。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

可选。

图像服务所提供图像的URL。 如果URL不存在，则库使用在`src`属性中设置的值作为回退。 此属性用于响应式图像库从不同位置管理的初始图像和动态图像。

**示例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

如果设置了`data-src`，则`src`为可选项，并且可以包含要添加的任何URL。 例如，它可以包含指向库使用的同一基于图像服务的图像的URL。 或者，它可以包含GIF占位符，甚至可以包含数据URI，以避免在启动时出现额外的服务器往返。

如果未设置`data-src`，则`src`为必填项，并且必须包含图像服务所提供图像的URL。

**示例**

使用`src`属性的数据URI和`data-src`属性的图像服务URL:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗号分隔的断点列表，后跟冒号(`:`)和图像服务命令或图像预设（可选）。 每个断点是在逻辑CSS像素中定义的图像宽度值。 库从列表加载具有最大值的图像，并在客户端上缩小图像以匹配运行时CSS图像宽度。 （如果您在高密度屏幕上工作，则从服务器加载的图像演绎版表示断点值与设备的像素比相乘。）

对于列表中的任何断点，可以定义一个或多个图像服务命令或图像预设名称。 此类额外参数仅应用于图像，以防此特定断点当前处于活动状态。

除了那些影响响应图像大小的视图命令（如`wid=`、`hei=`或`scl=`）外，可以使用任何受支持的图像服务命令。 同样的限制也适用于图像预设：与响应式图像库一起使用的图像预设不能包含此类命令。

多个图像服务命令或图像预设名称以&quot; `&`&quot;字符分隔。 如果图像服务命令的值中包含逗号，则此逗号将替换为`%2C`。 图像预设名称用美元符号(`$`)封装。

**示例**

**仅使用断点**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用图像服务命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用图像预设**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用图像预设和图像服务命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4及更高版本和Dynamic Media Viewer 5.9及更高版本中提供以下两种智能裁剪模式：

* **手动**  — 用户定义的断点和相应的图像服务命令是在图像元素的属性中定义的。
* **智能裁剪**  — 从投放服务器自动检索计算的智能裁剪演绎版。使用图像元素的运行时大小选择最佳再现。

要使用“智能裁剪”模式，请将`data-mode`属性设置为`smart crop`。

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

