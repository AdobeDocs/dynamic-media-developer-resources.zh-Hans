---
description: 蒙版图像的一部分。 蒙版始终与图像相关联。 从ImageInfo获取蒙版。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e18096c-0666-400b-a562-b6d183bd3334
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 8%

---

# [!DNL Mask]{#mask}

蒙版图像的一部分。 蒙版始终与图像相关联。 从ImageInfo获取蒙版。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| maskHandle | `xsd:string` | 蒙版手柄。 |
| 名称 | `xsd:string` | 蒙版名称。 |
| 蒙版路径 | `xsd:string` | 蒙版的相对路径。 |
| 蒙版文件 | `xsd:string` | 蒙版文件。 |
| lastModified | `types:dateTime` | 上次修改掩码的日期、时间和时区。 |
