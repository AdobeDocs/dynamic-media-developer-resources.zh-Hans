---
description: 层按layer=命令指定的顺序合成，其中较高编号的层隐藏较低编号的层。
solution: Experience Manager
title: 复合画布
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 复合画布{#the-compositing-canvas}

层按layer=命令指定的顺序合成，其中较高编号的层隐藏较低编号的层。

层0构成背景层，背景层始终是必需的，它定义了复合图像的大小。 层0允许任何层类型。 必须根据内容图像或文本显式地使用`size=`或隐式地定义层0的大小。 位于第0层区域之外的其它层区域将不会包含在输出图像中。

>[!NOTE]
>
>在对所有层进行扁平化之后，复合图像将转换为最终响应图像，这与[view命令和属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)一起指定。
