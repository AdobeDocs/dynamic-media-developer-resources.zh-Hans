---
description: 为指定的资产设置“图像提供”或“图像呈现”协议命令。 这些命令可修改资产的表示形式，而不会破坏资产。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

为指定的资产设置“图像提供”或“图像呈现”协议命令。 这些命令可修改资产的表示形式，而不会破坏资产。

对于“图像提供”，`urlModifier`参数中的命令会发布在修饰符目录字段中，并在请求URL中指定的任何命令之前应用。 `urlPostApplyModifier`中的命令将发布到`PostModifier`目录字段，并将覆盖请求URL或`urlModifier`中的任何命令。 对于“图像渲染”，将连接`urlModifier`和`urlPostApplyModifier`中的命令并将其发布到修饰符目录字段。

## 授权用户类型 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input(setUrlModifierParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`urlModifier`*` | `xsd:string` | 否 | 在请求或`urlPostApplyModifier`命令之前应用的图像提供或图像呈现协议命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 要在`urlModifier`和请求命令之后应用的图像提供或图像呈现协议命令。 |

**Output(setUrlModifierReturn)**

IPS API不会返回此操作的响应。

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
