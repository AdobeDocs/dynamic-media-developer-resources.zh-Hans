---
description: 遮罩图像的一部分。 蒙版始终与图像关联。 从ImageInfo获取蒙版。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 0e18096c-0666-400b-a562-b6d183bd3334
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 13%

---

# 蒙版{#mask}

遮罩图像的一部分。 蒙版始终与图像关联。 从ImageInfo获取蒙版。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`maskHandle`*` | `xsd:string` | 口罩手柄。 |
| `*`name`*` | `xsd:string` | 掩码名称。 |
| `*`maskPath`*` | `xsd:string` | 蒙版的相对路径。 |
| `*`maskFile`*` | `xsd:string` | 蒙版文件. |
| `*`lastModified`*` | `types:dateTime` | 上次修改掩码的日期、时间和时区。 |
