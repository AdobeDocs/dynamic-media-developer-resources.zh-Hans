---
description: 分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。
solution: Experience Manager
title: 文件夹
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# 文件夹{#folder}

分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 文件夹句柄。 |
| `*`路径`*` | `xsd:string` | 文件夹路径。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改日期。 |
| `*`childLastModified`*` | `xsd:dateTime` | 子文件夹和文件夹子资产的上次修改日期。 |
| `*`permissionsSetHandle`*` | `xsd:string` | 文件夹权限句柄。 |
| `*`hasSubfolder`*` | `types:Boolean` | 确定文件夹是否包含子文件夹。 |
| `*`subfolderArray`*` | `types:FolderArray` | 文件夹中的子文件夹数组。 |
