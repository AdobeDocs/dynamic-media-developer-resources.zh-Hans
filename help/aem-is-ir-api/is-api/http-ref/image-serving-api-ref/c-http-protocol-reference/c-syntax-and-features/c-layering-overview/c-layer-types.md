---
description: 支持四种类型的层。
solution: Experience Manager
title: 图层类型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 图层类型{#layer-types}

支持四种类型的层。

## 图像图层 {#section-3e53df1437694272aca03f927fc0db07}

图像图层必须具有 `src=` 命令，指定用作图层的图像。 可以使用指定单独的图像 `mask=` 用作图层蒙版，或者图像可能已有Alpha通道。 图像图层的大小始终从图像派生，但图像通常会缩放以适合使用 `size=` 命令。 剪辑路径可以应用到 `clipPath=`.

## 文本图层 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必须具有 `text=` 或 `textPs=` 以富文本格式(RTF)文本片段的形式提供文本内容的命令。 文本图层可以根据内容自行调整大小，也可以指定明确的大小（例如，如果文本要换行到特定宽度，或者文本必须限制在特定区域中）。 `textPs=` 支持将文本流动为定义的任意形状 `textFlowPath=` 和到定义的任意路径 `textPath=`. `textPs=` 还支持将文本以任意角度渲染到文本框或指定形状中( `textAngle=`)。

## 纯色图层 {#section-56dfb672756643dda08dc93294809eb0}

纯色图层通常用于模板中的图层0，因此复合图像的大小是固定的，并且与任何图像内容无关。 纯色图层需要 `color=` 属性，以及 `size=` 或 `mask=`和支持大多数其他命令和属性来修改外观。 纯色图层可以具有任意形状 `clipPath=`.

## 效果图层 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop样式图层效果（如投影、发光效果）由IS使用特殊子图层实现，这些子图层可以附加到图像、文本和纯色图层。 这些效果图层继承父图层蒙版和父图层的位置，并且功能有限。
