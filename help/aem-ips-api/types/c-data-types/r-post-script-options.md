---
description: PostScript文件选项。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 进度 | `xsd:string` | PostScript进程选择。 |
| 解析度 | `xsd:double` | 文件解析。 |
| 颜色空间 | `xsd:string` | PostScript Colorspace模式。 |
| alpha | `xsd:boolean` | 是否将文件栅格化为图像。 如果是，则如果以这种方式定义原始文件，它将创建透明背景。 通常用于创建覆盖徽标。 |
| extractSearchWords | `xsd:boolean` | 是否从PostScript文件中提取搜索词。 |
