---
description: 建立衍生自現有主要來源影像資產的新資產。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

建立衍生自現有主要來源影像資產的新資產。

语法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

衍生資產會指定影像伺服器通訊協定命令，以修改擁有者影像的表示方式。 此 `AdjustedView` 衍生型別有助於將簡單的修改套用至單一影像（例如，藉由指定裁切矩形），而 `LayerView` 可協助建立包含文字或其他影像的多層檢視。

與影像復本不同(請參閱 [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))，則衍生影像會連結至其擁有者影像。 所有者影像的變更會修改關聯的衍生資產。 刪除擁有者影像將會刪除任何相關聯的衍生影像。

## 授權的使用者型別 {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-5a0dde01cff6454da3646ea805c2be1e}

**輸入(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要衍生新資產的資產的公司的控制代碼。 |
| ownerHandle | `xsd:string` | 是 | 衍生新影像的主要影像資產的控點。 |
| folderHandle | `xsd:string` | 是 | 建立新衍生資產的資料夾的控制代碼。 |
| 名称 | `xsd:string` | 是 | 衍生資產的名稱。 |
| 类型 | `xsd:string` | 是 | 新衍生資產的資產型別： `AdjustedView` 或 `LayerView`. |
| urlModifier | `xsd:string` | 否 | 已套用影像伺服或影像演算通訊協定命令 *早於* 要求或 `urlPostApplyModifier` 命令。 |
| urlPostApplyModifier | `xsd:string` | 否 | 已套用影像伺服或影像演算通訊協定命令 *晚於* 至請求或 `urlPostApplyModifier` 命令。 |

**輸出(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 衍生資產的控點。 |

## 示例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

範常式式碼會建立具有已調整檢視的衍生資產，並 `urlModifier` 和 `urlPostApplyModifier` 具有任意值。 回應會傳回新衍生資產的控點。

**请求**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**响应**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
