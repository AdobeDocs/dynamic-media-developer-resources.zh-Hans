---
description: PostScript文件选项。
seo-description: PostScript文件选项。
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Scene7 Image Production System API
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostScriptOptions{#postscriptoptions}

PostScript文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`进度`*` | `xsd:string` | PostScript进程选择。 |
| ` *`分辨率`*` | `xsd:double` | 文件分辨率。 |
| ` *`颜色空间`*` | `xsd:string` | PostScript色彩空间模式。 |
| ` *`alpha`*` | `xsd:boolean` | 是否将文件栅格化为图像。 如果是，则如果以这种方式定义原始文件，它将创建透明背景。 通常用于创建叠加徽标。 |
| ` *`extractSearchWords`*` | `xsd:boolean` | 是否从PostScript文件中提取搜索词。 |

