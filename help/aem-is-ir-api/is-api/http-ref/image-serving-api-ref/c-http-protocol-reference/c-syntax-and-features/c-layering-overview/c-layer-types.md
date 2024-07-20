---
description: 支持四种类型的层。
solution: Experience Manager
title: 图层类型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 图层类型{#layer-types}

支持四种类型的层。

## 图像图层 {#section-3e53df1437694272aca03f927fc0db07}

图像图层必须具有`src=`命令，该命令指定要用作图层的图像。 可以使用`mask=`指定单独的图像以用作图层蒙版，或者该图像可能已经具有Alpha通道。 图像图层的大小始终从图像派生，但图像通常使用`size=`命令缩放以适合图像。 可以使用`clipPath=`应用剪辑路径。

## 文本图层 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必须具有`text=`或`textPs=`命令，该命令以富文本格式(RTF)文本片段的形式提供文本内容。 文本图层可以根据其内容自行调整大小，也可以为其指定显式大小。 例如，如果文本要换行到特定宽度，或者文本必须限制在特定区域中。 `textPs=`支持将文本流入使用`textFlowPath=`定义的任意形状，并流入使用`textPath=`定义的任意路径。 `textPs=`还支持以任意角度(`textAngle=`)将文本渲染到文本框或指定的形状。

## 纯色图层 {#section-56dfb672756643dda08dc93294809eb0}

纯色图层通常用于模板中的图层0，因此复合图像的大小是固定的，并且与任何图像内容无关。 纯色图层需要`color=`属性以及`size=`或`mask=`，并支持大多数其他命令和属性来修改外观。 可以为纯色图层指定带有`clipPath=`的任意形状。

## 效果图层 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop样式图层效果（如投影、发光效果）是使用特殊子图层通过IS实现的，这些子图层可以附加到图像、文本和纯色图层。 这些效果图层会继承父图层蒙版并从父图层进行定位，并且功能有限。
