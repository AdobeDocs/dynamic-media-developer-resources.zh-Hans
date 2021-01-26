---
description: 分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。
seo-description: 分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。
seo-title: 文件夹
solution: Experience Manager
title: 文件夹
topic: Dynamic Media Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '86'
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
| `*`childLastModified`*` | `xsd:dateTime` | 子文件夹和文件夹子资源的上次修改日期。 |
| `*`permissionsSetHandle`*` | `xsd:string` | 文件夹权限处理。 |
| `*`hasSubfolder`*` | `types:Boolean` | 确定文件夹是否包含子文件夹。 |
| `*`subfolderArray`*` | `types:FolderArray` | 文件夹中的子文件夹的数组。 |

