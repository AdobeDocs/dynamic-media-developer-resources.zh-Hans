---
title: emptyAssetsFromTrash
description: 清空IPS垃圾桶中的資產。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 8%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

清空IPS垃圾桶中的資產。

資產會一直留在垃圾桶中，直到手動清空或逾時。 如果手動清空，它們會留在垃圾桶中，直到最後從系統中清除時為止（通常是在夜間）。 如果資產在垃圾桶中逾時，系統會在該清理活動中清理資產。 可設定逾時（預設為7天）。

## 授權的使用者型別 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8e1fb0ee3aae453581e99ef76e298569}

**輸入(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | xsd:string | 是 | 擁有資產的公司的控制代碼。 |
| assetHandleArray | 型別：HandleArray | 是 | 代表要從垃圾桶清空之專案的控點陣列。 |

**輸出(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | xsd：Int | 是 | 已成功從垃圾桶清空的資產數量。 |
| warningCount | xsd：Int | 是 | 作業嘗試從垃圾桶清空資產時產生的警告數目。 |
| errororcount | xsd：Int | 是 | 作業嘗試從垃圾桶清空資產時產生的錯誤數。 |
| warningDetailArray | 型別：AssetOperationFaultArray | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試從垃圾桶清空資產時產生警告。 |
| errorDetailArray | 型別：AssetOperationFaultArray | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試從垃圾桶清空資產時產生錯誤。 |

## 示例 {#section-6154a873b6c342bf92e2036280cafdcf}

此程式碼範例使用公司的控制代碼和資產控制代碼陣列，其中包含要從垃圾桶清空的資產控制代碼。

**请求**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**响应**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
