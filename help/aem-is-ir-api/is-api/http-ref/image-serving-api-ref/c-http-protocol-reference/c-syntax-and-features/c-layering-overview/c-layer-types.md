---
description: 支持四种类型的层。
solution: Experience Manager
title: 图层类型
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 图层类型{#layer-types}

支持四种类型的层。

## 图像图层 {#section-3e53df1437694272aca03f927fc0db07}

图像层必须具有`src=`命令，该命令指定要用作层的图像。 可以使用`mask=`指定单独的图像作为层掩模，或者该图像可能已经具有Alpha通道。 图像层的大小始终由图像派生，但图像通常会使用`size=`命令缩放以适合。 可以使用`clipPath=`应用剪辑路径。

## 文本图层 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必须具有`text=`或`textPs=`命令，该命令以富文本格式(RTF)文本片段的形式提供文本内容。 文本层可以根据其内容自行调整大小，也可以指定明确的大小（例如，如果文本要封装到特定宽度，或者文本必须限制在特定区域内）。 `textPs=` 支持将文本流入通过定义的任意形状， `textFlowPath=` 并流入通过定义的任意路 `textPath=`径。`textPs=` 还支持将文本渲染到文本框或指定形状中任意角度( `textAngle=`)。

## 纯色层 {#section-56dfb672756643dda08dc93294809eb0}

模板中的图层0通常使用实色层，因此复合图像的大小是固定的，并且与任何图像内容无关。 实色层需要`color=`属性以及`size=`或`mask=`，并且支持大多数其他命令和属性来修改外观。 实色层可以具有`clipPath=`的任意形状。

## 效果层 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop样式的图层效果（如投影和发光效果）由IS使用可附加到图像、文本和纯色层的特殊子层来实现。 这些效果层会从父层继承父层蒙版和位置，并且在功能上受到限制。
