---
description: 创建从现有的主源图像资源派生的新资源。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

创建从现有的主源图像资源派生的新资源。

语法

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生资源指定用于修改所有者图像表示法的图像服务器协议命令。 `AdjustedView`派生类型有助于将简单的修改应用于单个图像（例如，通过指定裁切矩形），而`LayerView`可帮助创建可能包含文本或其他图像的多层视图。

与图像副本（请参阅[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)）不同，派生图像已链接到其所有者图像。 更改所有者图像会修改关联的派生资源。 删除所有者映像将删除任何关联的派生映像。

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
| companyHandle | `xsd:string` | 是 | 包含新资产的公司的句柄，从该资产衍生新资产。 |
| ownerHandle | `xsd:string` | 是 | 从中派生新图像的主图像资源的句柄。 |
| folderHandle | `xsd:string` | 是 | 在其中创建新派生资源的文件夹的句柄。 |
| 名称 | `xsd:string` | 是 | 派生资源的名称。 |
| 类型 | `xsd:string` | 是 | 新派生资源的资源类型： `AdjustedView`或`LayerView`。 |
| urlModifier | `xsd:string` | 否 | 图像服务或图像渲染协议命令在&#x200B;*请求或`urlPostApplyModifier`命令之前应用了*&#x200B;个。 |
| urlPostApplyModifier | `xsd:string` | 否 | 图像服务或图像渲染协议命令在&#x200B;*之后*&#x200B;应用于请求或`urlPostApplyModifier`命令。 |

**输出(createDerivedAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 派生资源的句柄。 |

## 示例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

示例代码创建一个派生资源，该资源具有已调整的视图以及具有任意值的`urlModifier`和`urlPostApplyModifier`。 响应会将句柄返回到新派生的资产。

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
