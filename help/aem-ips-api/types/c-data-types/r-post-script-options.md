---
description: PostScript文件选项。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 进度 | `xsd:string` | PostScript进程选择。 |
| 解析度 | `xsd:double` | 文件解析。 |
| 颜色空间 | `xsd:string` | PostScript色彩空间模式。 |
| alpha | `xsd:boolean` | 是否将文件栅格化为图像。 如果是这样，如果以这种方式定义了原始文件，则它会创建一个透明背景。 通常用于创建叠加徽标。 |
| extractSearchWords | `xsd:boolean` | 是否从PostScript文件中提取搜索词。 |
