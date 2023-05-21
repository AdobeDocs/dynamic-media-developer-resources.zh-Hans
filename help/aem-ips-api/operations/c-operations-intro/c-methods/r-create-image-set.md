---
description: 建立影像集。
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 15%

---

# createImageSet{#createimageset}

建立影像集。

语法

## 授權的使用者型別 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有目的地資料夾的讀取/寫入存取權。

## 参数 {#section-03d22ba7d290477e91c25ca1d4439200}

**輸入(createImageSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 影像集所屬公司的控制代碼。 |
| folderHandle | `xsd:string` | 是 | 資料夾的控制代碼。 |
| 名称 | `xsd:string` | 是 | 影像集名稱。 |
| 类型 | `xsd:string` | 是 | 影像集型別。 |
| thumbAssetHandle | `xsd:string` | 否 | 資產的控制代碼，可作為新影像集的縮圖。 如果未指定，IPS會嘗試使用集合所參考的第一個影像資產。 |

**輸出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 新影像集的操作框。 |

## 示例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此程式碼範例會建立由公司、資料夾、名稱和型別指定的影像集。 回應是新建立影像集的資產控制代碼。

**请求**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**响应**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
