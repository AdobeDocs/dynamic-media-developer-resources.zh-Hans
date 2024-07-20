---
description: 为指定的资产设置图像服务或图像渲染协议命令。 这些命令可修改资源的表示形式而不会破坏资源。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

为指定的资产设置图像服务或图像渲染协议命令。 这些命令可修改资源的表示形式而不会破坏资源。

对于图像提供，`urlModifier`参数中的命令在修饰符目录字段中发布，并在请求URL上指定的任何命令之前应用。 `urlPostApplyModifier`中的命令已发布到`PostModifier`目录字段，并覆盖请求URL或`urlModifier`中的任何命令。 对于图像渲染，`urlModifier`和`urlPostApplyModifier`中的命令连接并发布到修饰符目录字段。

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
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| assetHandle | `xsd:string` | 是 | 资产句柄。 |
| urlModifier | `xsd:string` | 否 | 在请求或`urlPostApplyModifier`命令之前应用的图像提供或图像渲染协议命令。 |
| urlPostApplyModifier | `xsd:string` | 否 | 在`urlModifier`和请求命令之后应用的图像提供或图像渲染协议命令。 |

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
