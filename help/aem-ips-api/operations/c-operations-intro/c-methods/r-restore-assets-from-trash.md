---
description: 從垃圾桶還原資產。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 12%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

從垃圾桶還原資產。

语法

## 授權的使用者型別 {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-200a61d040c94e489a85241b29cd499a}

**輸入(restoreAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 擁有您要還原之資產的公司的控制代碼。 |
| assetHandleArray | `types:HandleArray` | 是 | 您要還原之資產的控點陣列。 |

**輸出(restoreAssetsFromTrashReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功從垃圾桶移除的資產數量。 |
| warningCount | `xsd:int` | 是 | 作業嘗試從垃圾桶還原資產時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 嘗試從垃圾桶還原資產時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試從垃圾桶還原資產時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試從垃圾桶還原資產時產生錯誤。 |

## 示例 {#section-98fe0394b0634ca397c395f14f8a9358}

此程式碼範例會從垃圾桶還原資產。 回應指出作業已順利完成。

**请求**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**响应**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
