---
description: 傳回階層樹狀結構中的資料夾和子資料夾。 getFolderTree回應最多只能有100,000個資料夾
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

傳回階層樹狀結構中的資料夾和子資料夾。 getFolderTree回應最多只能有100,000個資料夾

语法

## 授權的使用者型別 {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾的讀取存取權才能傳回其上的資料。

## 参数 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**輸入(getFolderTreeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| accessUserHandle | `xsd:string` | 否 | 僅供管理員用來模擬特定使用者。 |
| accessGroupHandle | `xsd:string` | 否 | 用於依特定群組篩選，包括公司所屬的任何群組。 |
| 資料夾路徑 | `xsd:string` | 否 | 根資料夾，可擷取葉層級的資料夾和所有子資料夾。 如果排除，則使用公司根目錄。 |
| 深度 | `xsd:int` | 是 | 值為零會取得頂層資料夾。 任何其他值都會指定下降到樹狀結構中的深度。 |
| assetTypeArray | `types:StringArray` | 否 | 傳回僅包含指定資產型別的資料夾。 |
| responseFieldArray | `types:StringArray` | 否 | 包含您要包含在回應中的欄位清單。 |
| excludeFieldArray | `types:StringArray` | 否 | 包含您要在回應中排除的欄位清單。 |

**輸出(getFolderTreeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 文件夹 | `types:folders` | 否 | 樹狀結構中的資料夾階層。 回應最多可包含100,000個資料夾。 |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 示例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

此程式碼範例使用公司控制代碼和深度引數來決定回應應傳回的深度等級。 回應包含具有相關性的資料夾和子資料夾陣列。 將深度值設為較小的數字，以便在資料夾樹狀結構中更深入地進行搜尋。

**请求**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**响应**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
