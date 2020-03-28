---
description: 支持四种类型的图层。
seo-description: 支持四种类型的图层。
seo-title: 图层类型
solution: Experience Manager
title: 图层类型
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图层类型{#layer-types}

支持四种类型的图层。

## 图像图层 {#section-3e53df1437694272aca03f927fc0db07}

图像图层必须有 `src=` 一个命令，该命令指定要用作图层的图像。 可以指定单独的图像以用 `mask=` 作图层蒙版，或者该图像可能已具有alpha渠道。 图像图层的大小始终从图像派生，但通常使用命令缩放图像以适合 `size=` 大小。 可以应用剪辑路径 `clipPath=`。

## 文本图层 {#section-dc2aec6416a340bcb20c1f884323c8d0}

必须具有 `text=` 或命 `textPs=` 令，该命令以富文本格式(RTF)文本片段的形式提供文本内容。 文本图层可以根据其内容自动调整大小，也可以指定明确大小（例如，如果文本要绕排到特定宽度，或者文本必须限制在特定区域内）。 `textPs=` 支持将文本流入使用定义的任意形状，并 `textFlowPath=` 且流入使用定义的任意路径 `textPath=`。 `textPs=` 还支持将文本渲染到文本框或指定的形状中，以任意角度( `textAngle=`)显示。

## 纯色图层 {#section-56dfb672756643dda08dc93294809eb0}

纯色图层通常用于模板中的图层0，因此复合图像的大小是固定的并且与任何图像内容无关。 纯色图层需要一 `color=` 个属性，并且或 `size=` 支 `mask=`持大多数其他命令和属性来修改外观。 可以将纯色图层赋予任意形状 `clipPath=`。

## 效果图层 {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop样式的图层效果（如投影和发光效果）由IS使用可附加到图像、文本和纯色图层的特殊子图层来实现。 这些效果图层继承父图层蒙版和父图层的位置，并且功能有限。
