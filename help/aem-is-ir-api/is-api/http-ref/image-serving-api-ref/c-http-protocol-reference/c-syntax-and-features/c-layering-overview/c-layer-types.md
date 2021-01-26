---
description: 支持四种类型的图层。
seo-description: 支持四种类型的图层。
seo-title: 图层类型
solution: Experience Manager
title: 图层类型
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# 层类型{#layer-types}

支持四种类型的图层。

## 图像层{#section-3e53df1437694272aca03f927fc0db07}

图像图层必须具有`src=`命令，该命令指定要用作图层的图像。 可以用`mask=`指定单独的图像以用作图层蒙版，或者该图像可能已具有alpha渠道。 图像图层的大小始终从图像中派生，但通常使用`size=`命令缩放图像以适合。 剪辑路径可以与`clipPath=`一起应用。

## 文本层{#section-dc2aec6416a340bcb20c1f884323c8d0}

必须具有`text=`或`textPs=`命令，该命令以富文本格式(RTF)文本片段的形式提供文本内容。 文本图层可以根据其内容自行调整大小，也可以给出明确大小（例如，如果文本要绕排到特定宽度，或者文本必须限制在特定区域内）。 `textPs=` 支持将文本流入用定义的任意形状 `textFlowPath=` 中，并流入用定义的任意路径 `textPath=`。`textPs=` 还支持将文本渲染到文本框中或以任意角度( `textAngle=`)指定形状。

## 纯色层{#section-56dfb672756643dda08dc93294809eb0}

纯色图层通常用于模板中的图层0，因此复合图像的大小是固定的，并且与任何图像内容无关。 纯色图层需要`color=`属性和`size=`或`mask=`，并且支持大多数其他命令和属性来修改外观。 固态色层可以具有`clipPath=`的任意形状。

## 效果层{#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop风格的图层效果（如投影和发光效果）由IS使用特殊的子图层实现，这些子图层可附加到图像、文本和纯色图层。 这些效果图层继承父图层的蒙版和位置，并且功能受到限制。
