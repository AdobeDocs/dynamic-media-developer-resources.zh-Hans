---
description: 创建从现有主源图像资产派生的新资产。
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

创建从现有主源图像资产派生的新资产。

语法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生资产指定用于修改所有者图像表示的图像服务器协议命令。 的 `AdjustedView` 派生类型有助于对单个图像应用简单的修改（例如，通过指定裁剪矩形），而 `LayerView` 有助于创建可能包含文本或其他图像的多层视图。

与图像副本不同(请参阅 [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))，则派生的图像会链接到其所有者图像。 对所有者图像所做的更改会修改关联的派生资产。 删除所有者图像将删除任何关联的派生图像。

## 授权用户类型 {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-5a0dde01cff6454da3646ea805c2be1e}

**输入(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要从中获取新资产的资产的公司句柄。 |
| ownerHandle | `xsd:string` | 是 | 从中派生新图像的主图像资产的句柄。 |
| folderHandle | `xsd:string` | 是 | 创建新派生资产的文件夹的句柄。 |
| name | `xsd:string` | 是 | 派生资产的名称。 |
| 类型 | `xsd:string` | 是 | 新派生资产的资产类型： `AdjustedView` 或 `LayerView`. |
| urlModifier | `xsd:string` | 否 | 应用图像提供或图像呈现协议命令 *之前* 请求或 `urlPostApplyModifier` 中。 |
| urlPostApplyModifier | `xsd:string` | 否 | 应用图像提供或图像呈现协议命令 *after* 请求或 `urlPostApplyModifier` 中。 |

**输出(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 派生资产的句柄。 |

## 示例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

示例代码创建具有调整视图和 `urlModifier` 和 `urlPostApplyModifier` 任意值。 响应会将句柄返回到新派生的资产。

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
