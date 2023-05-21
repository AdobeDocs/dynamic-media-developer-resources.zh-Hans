---
description: 階層式檔案或資產儲存物件。 資料夾可以包含一個（或多個）子資料夾。
solution: Experience Manager
title: 文件夹
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---

# [!DNL Folder]{#folder}

階層式檔案或資產儲存物件。 資料夾可以包含一個（或多個）子資料夾。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| folderHandle | `xsd:string` | 資料夾控制代碼。 |
| [!DNL path] | `xsd:string` | 資料夾路徑。 |
| lastModified | `xsd:dateTime` | 上次修改日期。 |
| childLastModified | `xsd:dateTime` | 子資料夾和資料夾子資產的上次修改日期。 |
| permissionsSetHandle | `xsd:string` | 檔案夾許可權控制代碼。 |
| hasSubfolder | `types:Boolean` | 決定資料夾是否有子資料夾。 |
| subfolderarray | `types:FolderArray` | 資料夾中的子資料夾陣列。 |
