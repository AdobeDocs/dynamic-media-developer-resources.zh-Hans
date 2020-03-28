---
description: 为指定的资产设置图像服务或图像渲染协议命令。 这些命令可修改资产的表示形式，而不会破坏它。
seo-description: 为指定的资产设置图像服务或图像渲染协议命令。 这些命令可修改资产的表示形式，而不会破坏它。
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

为指定的资产设置图像服务或图像渲染协议命令。 这些命令可修改资产的表示形式，而不会破坏它。

对于图像服务，参数中的命 `urlModifier` 令将发布在修饰符目录字段中，并在请求URL上指定的任何命令之前应用。 中的命 `urlPostApplyModifier` 令将发布到目 `PostModifier` 录字段，并将覆盖请求URL或中的任何命令 `urlModifier`。 对于“图像渲染”，将连接和 `urlModifier` 中的 `urlPostApplyModifier` 命令并将其发布到修饰符目录字段。

## 授权用户类型 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**输入(setUrlModifierParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| ` *`urlModifier`*` | `xsd:string` | 否 | 在请求或命令之前应用的图像服务或图像渲染协议 `urlPostApplyModifier` 命令。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 否 | 在和请求命令后应用的图像服务或图像渲 `urlModifier` 染协议命令。 |

**输出(setUrlModifierReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-801d4b9b986443f59a5783a3d6bf44aa}

**请求**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**响应**

无。
