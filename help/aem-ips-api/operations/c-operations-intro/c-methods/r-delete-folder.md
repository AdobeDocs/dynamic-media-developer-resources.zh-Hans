---
description: 刪除資料夾。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# deleteFolder{#deletefolder}

刪除資料夾。

语法

## 授權的使用者型別 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資料夾及其所有子項的讀取和刪除存取權。

## 参数 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**輸入(deleteFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資料夾所屬公司的控制代碼。 |
| folderHandle | `xsd:string` | 是 | 要刪除的資料夾的控制代碼。 |

**輸出(deleteFolderParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-9d4617b322e8442d80e59be0f8714841}

此程式碼範例會從公司的根目錄中刪除資料夾。 它需要資料夾控制代碼，您必須從其他作業取得此控制代碼。

**请求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

无。
