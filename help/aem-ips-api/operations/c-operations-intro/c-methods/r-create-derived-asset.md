---
description: 创建从现有主源图像资产派生的新资产。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

创建从现有主源图像资产派生的新资产。

语法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生资源指定用于修改所有者图像表示的图像服务器协议命令。 `AdjustedView`派生类型有助于对单个图像应用简单的修改（例如，通过指定裁剪矩形），而`LayerView`有助于创建可能包含文本或其他图像的多图层视图。

与图像副本（请参阅[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)）不同，派生的图像将链接到其所有者图像。 对所有者图像的更改将修改关联的派生资产。 删除所有者图像将删除任何关联的派生图像。

## 授权用户类型{#authorized-user-types}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要从中派生新资产的资产的公司的句柄。 |
| `*`ownerHandle`*` | `xsd:string` | 是 | 将从中派生新图像的主图像资产的句柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 将在其中创建新派生资产的文件夹的句柄。 |
| `*`name`*` | `xsd:string` | 是 | 派生资产的名称。 |
| `*`类型`*` | `xsd:string` | 是 | 新派生资产的资产类型：`AdjustedView`或`LayerView`。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 在&#x200B;*请求或`urlPostApplyModifier`命令之前应用了*&#x200B;的图像服务或图像渲染协议命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 对请求或`urlPostApplyModifier`命令应用&#x200B;*之后的图像服务或图像渲染协议命令。* |

**输出(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 派生资产的句柄。 |

## 示例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

示例代码创建一个具有调整视图和具有任意值的`urlModifier`和`urlPostApplyModifier`的派生资产。 该响应将返回新派生资产的句柄。

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

