---
description: 创建“纸娃娃”分层应用程序。
seo-description: 创建“纸娃娃”分层应用程序。
seo-title: 示例C
solution: Experience Manager
title: 示例C
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# 示例C{#example-c}

创建“纸娃娃”分层应用程序。

背景图像包含模型或人体模型的照片。 图像目录中的其他记录包含各种服装和附件项目，拍摄这些项目是为了使模特道具的形状和大小与模特道具相匹配。

每张服装/附件照片都会被蒙版并裁剪到蒙版定界框，以最大限度地减小图像大小。 仔细控制图像锚点和分辨率以保持图层和背景图像之间的对齐，并将所有图像添加到图像目录中，并将相应值存储在`catalog::Resolution`和`catalog::Anchor`中。

除了分层之外，我们还要更改选定项目的颜色。 对这些项的记录进行预处理以去除原始颜色并以适合于着色命令的方式调整亮度和对比度。 此预处理可以离线完成，使用Photoshop等图像编辑工具；在简单情况下，可以通过向`catalog::Modifier`字段添加`op_brightness=`和`op_contrast=`来逐步完成。

此应用程序不保证单独的模板，因为所有对象已通过其图像锚点(`catalog::Anchor`)正确对齐，并且缩放(`catalog::Resolution`)。 我们将由客户端负责确保适当的图层顺序。

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

只指定高度。 这样，返回的图像就会根据人体模型图像的长宽比而在宽度上发生变化，而不会得到用背景颜色填充的边距。

只要每个图层都相同，为每个图层指定的分辨率就不重要。 此版本可能不允许视图大于合成图像。 指定大分辨率值可避免与此限制相关的问题。 所有处理和合成都以所请求图像大小的最佳分辨率完成，以帮助获得最佳性能和输出质量。

如果所有源图像的分辨率都完全相同（这很可能适用于此类应用程序），则可省略`res=`命令。

必须为所有`src=`命令指定`rootId`，即使这些命令与url路径中指定的`rootId`相同。

如果不使用图像目录，则无法使用基于分辨率的缩放方法。 在这种情况下，必须根据每个图层的`catalog::Resolution`值与背景图层的`catalog::Resolution`值的比值，为每个图层项计算显式缩放系数。 因此，合成请求（图层数较少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

