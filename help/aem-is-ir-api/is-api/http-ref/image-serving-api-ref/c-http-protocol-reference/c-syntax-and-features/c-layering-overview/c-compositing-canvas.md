---
description: 按照layer=命令指定的顺序合成图层，其中编号较高的图层隐藏编号较低的图层。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# 合成画布{#the-compositing-canvas}

按照layer=命令指定的顺序合成图层，其中编号较高的图层隐藏编号较低的图层。

图层0构成背景图层，背景图层始终是必需的，用于定义复合图像的大小。 第0层允许使用任何层类型。 必须使用显式定义层0的大小 `size=` 或者，隐式地，基于内容图像或文本。 其他图层中落在图层0区域之外的任何区域都不会包含在输出图像中。

>[!NOTE]
>
>将所有图层平面化后，复合图像将转换为最终响应图像，如使用 [查看命令和属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
