---
title: 示例C
description: 创建一个“纸娃娃”分层应用程序。
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

创建一个“纸娃娃”分层应用程序。

背景图像包含模型或人体模型的照片。 图像目录中的其他记录包含各种服装和配件，拍摄它们以匹配人体模型的形状和大小。

每个服装/附件照片被遮罩并裁剪到遮罩边界框以最小化图像大小。 仔细控制图像锚点和分辨率以保持图层与背景图像之间的对齐，并且所有图像都添加到图像目录中，相应的值存储在`catalog::Resolution`和`catalog::Anchor`中。

除了分层外，您还需要更改所选项目的颜色。 对这些项目的记录进行预处理，以去除原始颜色，并以适合彩色化命令的方式调整亮度和对比度。 此预处理可以使用图像编辑工具(如Adobe Photoshop)离线完成，或者在简单情况下，可以通过将`op_brightness=`和`op_contrast=`添加到`catalog::Modifier`字段来逐个完成。

此应用程序不保证使用单独的模板，因为所有对象已由其图像锚点( `catalog::Anchor`)正确对齐，并已缩放( `catalog::Resolution`)。 由客户端来确保适当的层顺序。

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

仅指定高度。 这样做可使返回的图像根据人体模型图像的纵横比而改变宽度，而不会获得填充了背景颜色的边距。

只要每个图层都相同，就不必为它们指定什么分辨率。 此版本可能不允许视图大于复合图像。 指定较大的分辨率值可避免与此限制相关的问题。 所有处理和合成均以所请求图像大小的最佳分辨率完成，以帮助实现最佳性能和输出质量。

如果所有源图像在全尺度上具有相同的分辨率，则可以省略`res=`命令（这有可能是这种类型的应用程序的情况）。

必须为所有`src=`命令指定`rootId`，即使它们与URL路径中指定的`rootId`相同。

如果不使用图像目录，则无法使用基于分辨率的缩放方法。 在这种情况下，必须根据每个图层的`catalog::Resolution`值与背景图层的`catalog::Resolution`值的比值，为每个图层项计算显式比例因子。 因此，复合请求（层数较少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
