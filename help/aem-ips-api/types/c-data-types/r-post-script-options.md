---
description: PostScript文件选项。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# PostScriptOptions{#postscriptoptions}

PostScript文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`进度`*` | `xsd:string` | PostScript进程选择。 |
| `*`resolution`*` | `xsd:double` | 文件解析。 |
| `*`颜色空间`*` | `xsd:string` | PostScript Colorspace模式。 |
| `*`alpha`*` | `xsd:boolean` | 是否将文件栅格化为图像。 如果是，则如果以这种方式定义原始文件，它将创建透明背景。 通常用于创建覆盖徽标。 |
| `*`extractSearchWords`*` | `xsd:boolean` | 是否从PostScript文件中提取搜索词。 |
