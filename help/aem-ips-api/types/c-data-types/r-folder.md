---
description: 分层文件或资源存储对象。 文件夹可以包含一个（或多个）子文件夹。
solution: Experience Manager
title: 文件夹
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# 文件夹{#folder}

分层文件或资源存储对象。 文件夹可以包含一个（或多个）子文件夹。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 文件夹句柄。 |
| `*`路径`*` | `xsd:string` | 文件夹路径。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改日期。 |
| `*`childLastModified`*` | `xsd:dateTime` | 子文件夹和文件夹子资源的上次修改日期。 |
| `*`permissionsSetHandle`*` | `xsd:string` | 文件夹权限处理。 |
| `*`hasSubfolder`*` | `types:Boolean` | 确定文件夹是否包含子文件夹。 |
| `*`subfolderArray`*` | `types:FolderArray` | 文件夹中的子文件夹数组。 |

