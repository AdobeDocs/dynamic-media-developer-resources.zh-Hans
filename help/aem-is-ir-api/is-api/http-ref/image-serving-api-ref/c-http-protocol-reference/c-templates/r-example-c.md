---
description: 创建“纸娃娃”分层应用程序。
solution: Experience Manager
title: 示例C
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 示例C{#example-c}

创建“纸娃娃”分层应用程序。

背景图像包含模型或人体模型的照片。 图像目录中的其他记录包含各种服装和配件，这些物品是为了与人体模型的形状和大小匹配而拍摄的。

每张服装/附件照片都被蒙版并被裁剪到蒙版定界框以最小化图像大小。 图像锚点和分辨率经过仔细控制以保持图层和背景图像之间的对齐，所有图像都被添加到图像目录中，并且相应的值存储在`catalog::Resolution`和`catalog::Anchor`中。

除了分层之外，我们还希望更改选定项目的颜色。 对这些项的记录进行预处理以去除原始颜色，并以适合着色命令的方式调整亮度和对比度。 此预处理过程可以通过使用图像编辑工具(如Photoshop)离线完成，或者在简单的情况下，也可以通过向`catalog::Modifier`字段添加`op_brightness=`和`op_contrast=`来逐步完成。

此应用程序不需要单独的模板，因为所有对象已通过其图像锚点(`catalog::Anchor`)正确对齐，并且已缩放(`catalog::Resolution`)。 我们将留给客户端来确保适当的层顺序。

典型的请求可能如下所示：

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

只指定高度。 这样，返回的图像宽度会因人体模型图像的宽高比而异，而不会获得用背景颜色填充的边距。

只要每个层都相同，就不应该指定什么分辨率。 此版本可能不允许视图大于复合图像。 指定大分辨率值可避免与此限制相关的问题。 所有处理和合成都以请求的图像大小的最佳分辨率完成，以帮助获得最佳性能和输出质量。

如果所有源图像的分辨率都完全相同（这可能是此类应用程序的情况），则可以忽略`res=`命令。

必须为所有`src=`命令指定`rootId`，即使它们与URL路径中指定的`rootId`相同。

如果不使用图像目录，则无法使用基于分辨率的缩放方法。 在这种情况下，必须根据每个层的`catalog::Resolution`值与背景层的`catalog::Resolution`值的比值，为每个层项目计算显式缩放因子。 因此，合成请求（层数较少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
