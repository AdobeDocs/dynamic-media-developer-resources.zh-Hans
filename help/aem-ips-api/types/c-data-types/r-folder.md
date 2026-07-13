---
description: 分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。
solution: Experience Manager
title: 文件夹
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 8%

---

# [!DNL Folder]{#folder}

分层文件或资产存储对象。 文件夹可以包含一个（或多个）子文件夹。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| folderHandle | `xsd:string` | 文件夹句柄。 |
| [!DNL path] | `xsd:string` | 文件夹路径。 |
| lastModified | `xsd:dateTime` | 上次修改日期。 |
| childLastModified | `xsd:dateTime` | 子文件夹和文件夹子资产的上次修改日期。 |
| permissionsSetHandle | `xsd:string` | 文件夹权限句柄。 |
| hasSubfolder | `types:Boolean` | 确定文件夹是否包含子文件夹。 |
| subfolderarray | `types:FolderArray` | 文件夹中的子文件夹数组。 |

