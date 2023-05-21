---
description: 從專案移除資產。 不會破壞資產。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# removeProjectAssets{#removeprojectassets}

從專案移除資產。 不會破壞資產。

语法

## 授權的使用者型別 {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-169d8e317417415b87df86242f65710e}

**輸入(removeProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 擁有您要移動之資產的公司的控制代碼。 |
| projectHandle | `xsd:string` | 是 | 您要移動之專案資產的控點。 |
| assetHandleArray | `types:HandleArray` | 是 | 您要移動之資產的控點陣列。 |

**輸出(removeProjectAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功移除資產計數。 |
| warningCount | `xsd:int` | 是 | 作業嘗試從專案移除資產時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試從專案移除資產時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試從專案移除資產時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在操作嘗試從專案中移除資產時產生錯誤。 |

## 示例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

此程式碼範例會從專案中移除2個資產（由專案控制代碼指定）。

**请求**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```
