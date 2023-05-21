---
description: 新增一或多個資產至專案。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# addProjectAssets{#addprojectassets}

新增一或多個資產至專案。

语法

## 授權的使用者型別 {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-20d498e971b6466298e60c8a77fc32b2}

**輸入(addProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 與目前專案關聯之公司的控制代碼。 |
| projectHandle | `xsd:string` | 是 | 處理您要新增資產的專案。 |
| projectHandlearray | `xsd:HandleArray` | 是 | 您要新增至目前專案的資產陣列。 |

**輸出(addProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功新增的資產數量。 |
| warningCount | `xsd:int` | 是 | 作業嘗試將資產新增至專案時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試將資產新增至專案時產生的錯誤數。 |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | 否 | 作業嘗試將資產新增至專案時，資產產生的一系列警告。 |
| companyHandle | `xsd:AssetOperationFaultArray` | 否 | 作業嘗試將資產新增至專案時，資產產生的錯誤陣列。 |

## 示例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此範例會將資產控制點陣列中的單一資產（由其控制點引用）新增至請求中指定的專案。 回應時，作業成功完成 `successCount` 傳回 `1`.

**请求**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**响应**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
