---
description: 從資料夾路徑開始，傳回所有資料夾和子資料夾。 getFolders回應最多會傳回100,000個資料夾。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

從資料夾路徑開始，傳回所有資料夾和子資料夾。 getFolders回應最多會傳回100,000個資料夾。

## 資料夾用途 {#section-66e344d5333f42f1b060a0cba25935c3}

資料夾可讓您組織子資料夾和資產。 所有資料夾和資產名稱必須是唯一的。 共用相同名稱的資料夾和資產會導致名稱空間衝突，即使它們位於不同的資料夾階層中亦然。
语法

## 授權的使用者型別 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾的讀取存取權才能傳回其上的資料。

## 参数 {#section-0c1976503eaa418a9226b51667901176}

**輸入(getFoldersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| accessUserHandle | `xsd:string` | 否 | 管理員用來模擬特定使用者。 |
| accessGroupHandle | `xsd:string` | 否 | 依特定群組篩選。 |
| 資料夾路徑 | `xsd:string` | 否 | 根資料夾，可擷取葉層級的資料夾和所有子資料夾。 如果排除，則使用公司根目錄。 |
| assetTypeArray | `types:StringArray` | 否 | 傳回僅包含指定資產型別的資料夾。 |
| responseFieldArray | `types:StringArray` | 否 | 包含您要包含在回應中的欄位清單。 |
| excludeFieldArray | `types:StringArray` | 否 | 包含您要從回應中排除的欄位清單。 |

**輸出(getFoldersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| folderArray | `types:FolderArray` | 否 | 符合篩選條件的資料夾陣列。 回應限製為最多100,000個資料夾。 |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## 示例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

此程式碼範例會傳回陣列，其中包含公司的所有資料夾以及有關每個資料夾的特定資訊。

**请求**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**响应**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
