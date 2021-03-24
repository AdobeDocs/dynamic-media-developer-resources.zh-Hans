---
description: 图层按图层=命令指定的顺序合成，其中较高编号的图层将隐藏较低编号的图层。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 合成画布{#the-compositing-canvas}

图层按图层=命令指定的顺序合成，其中较高编号的图层将隐藏较低编号的图层。

图层0构成背景图层，背景图层始终是必需的，它定义了复合图像的大小。 图层0允许任何图层类型。 必须根据内容图像或文本显式使用`size=`或隐式定义图层0的大小。 输出图像中不包括位于图层0区域之外的其他图层的任何区域。

>[!NOTE]
>
>拼合所有图层后，复合图像将转换为最终响应图像，如使用[视图命令和属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)指定的那样。

