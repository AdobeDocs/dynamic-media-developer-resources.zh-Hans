---
description: 重新命名資料夾。
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 22%

---

# renameFolder{#renamefolder}

重新命名資料夾。

语法

## 授權的使用者型別 {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 参数 {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**輸入(renameFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理具有您要重新命名資料夾的公司。 |
| folderHandle | `xsd:string` | 是 | 資料夾的控制代碼。 |
| folderName | `xsd:string` | 是 | 新資料夾名稱。 |

**輸出(renameFolderReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 重新命名資料夾的處理常式。 |

## 示例 {#section-98bdd2f88d164f488676e90aba1dc864}

此程式碼範例會重新命名資料夾。

**请求**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**响应**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
