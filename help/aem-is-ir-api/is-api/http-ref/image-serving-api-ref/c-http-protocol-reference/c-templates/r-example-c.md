---
description: 创建“纸娃娃”分层应用程序。
seo-description: 创建“纸娃娃”分层应用程序。
seo-title: 示例C
solution: Experience Manager
title: 示例C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 示例C{#example-c}

创建“纸娃娃”分层应用程序。

背景图像包含模型或人体模型的照片。 图像目录中的其他记录包含各种服饰和附件项目，拍摄这些项目是为了使模特的形状和大小与人体模型相匹配。

每张服装／附件照片都会被蒙版并裁剪到蒙版定界框，以最大限度地减小图像大小。 图像锚点和分辨率经过仔细控制以保持图层和背景图像之间的对齐，并且所有图像都会添加到图像目录中，并且会将相应的值存储在和 `catalog::Resolution` 中 `catalog::Anchor`。

除了分层，我们还要更改选定项目的颜色。 对这些项的记录进行预处理以去除原始颜色并以适合着色命令的方式调整亮度和对比度。 这种预处理可以离线完成，使用Photoshop等图像编辑工具，或者，在简单的情况下，可以通过向字段添加和添加到字段来 `op_brightness=` 实 `op_contrast=` 时地 `catalog::Modifier`完成。

此应用程序不保证单独的模板，因为所有对象已通过其图像锚点()和缩放( `catalog::Anchor`)正确对齐 `catalog::Resolution`了。 我们将其留给客户端来确保适当的图层顺序。

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

只指定高度。 这样，返回的图像宽度会因人体模型图像的长宽比而异，而不会填充背景颜色的边距。

只要每个图层都相同，就不应该指定哪个分辨率。 此版本可能不允许视图大于合成图像。 指定大分辨率值可避免与此限制相关的问题。 所有处理和合成都以所请求的图像大小的最佳分辨率进行，以帮助获得最佳性能和输出质量。

如果 `res=` 所有源图像的分辨率都完全相同（这很可能是这类应用程序的情况），则可以忽略这些命令。

必须 `rootId` 为所有命令指定，即 `src=` 使这些命令与url路径中指定 `rootId` 的命令相同。

如果不使用图像目录，则无法使用基于分辨率的缩放方法。 在这种情况下，必须根据每个图层的值与背景图层的值的比例，为每个图层项 `catalog::Resolution` 目计算显 `catalog::Resolution` 式缩放系数。 因此，合成请求（图层较少）可能如下所示：

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

