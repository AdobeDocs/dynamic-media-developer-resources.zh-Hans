---
title: 示例C
description: 创建“纸娃娃”分层应用程序。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 示例C{#example-c}

创建“纸娃娃”分层应用程序。

背景图像包含模型或人体模型的照片。 图像目录中的其他记录包含各种服装和配件，拍摄它们以匹配人体模型的形状和大小。

每个服装/附件照片都经过遮罩并裁剪到遮罩定界框以最小化图像大小。 仔细控制图像锚点和分辨率以保持图层与背景图像之间的对齐，并且所有图像都添加到图像目录中，相应的值存储在 `catalog::Resolution` 和 `catalog::Anchor`.

除了分层外，您还需要更改所选项目的颜色。 对这些项目的记录进行预处理，以去除原始颜色，并以适合彩色化命令的方式调整亮度和对比度。 此预处理可以使用图像编辑工具(如Adobe Photoshop)离线完成，或者在简单的情况下，可以通过添加以下各项逐一完成 `op_brightness=` 和 `op_contrast=` 到 `catalog::Modifier`字段。

此应用程序不保证使用单独的模板，因为所有对象都已由其图像锚点( `catalog::Anchor`)，并缩放( `catalog::Resolution`)。 由客户端来决定层顺序。

典型请求可能如下所示：

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

仅指定高度。 这样做可使返回的图像根据人体模型图像的长宽比而改变宽度，而不会得到用背景颜色填充的边距。

只要每个图层都一样，为每个图层指定何种分辨率应该无关紧要。 此版本可能不允许视图大于复合图像。 指定较大的分辨率值可避免与此限制相关的问题。 所有处理和合成都以所请求图像大小的最佳分辨率完成，以帮助实现最佳性能和输出质量。

此 `res=` 如果所有源图像在全尺度上具有相同的分辨率，则可以省略命令（这种类型的应用程序可能属于这种情况）。

此 `rootId` 必须为全部指定 `src=` 命令，即使它们与 `rootId` 在url路径中指定。

如果不需要使用图像目录，则无法使用基于分辨率的缩放方法。 在这种情况下，必须根据 `catalog::Resolution` 每个图层的值到 `catalog::Resolution` 背景图层的值。 因此，复合请求（层数较少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
