---
description: 删除缩放目标。
solution: Experience Manager
title: Deletzoomtarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 11%

---

# Deletzoomtarget{#deletezoomtarget}

删除缩放目标。

## 授权用户类型 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写访问权限。

## 参数 {#section-225330a45e7a408f8375e084677d9cb1}

**输入(deleteZoomTargetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 缩放目标所属公司的句柄。 |
| zoomTargetHandle | `xsd:string` | 是 | 要删除的缩放目标的句柄。 |

**输出(deleteZoomTargetParam)**

IPS API不返回此操作的响应。

## 示例 {#section-a35857a5ca884357a879f7ba6cf985fe}

此代码示例从公司删除缩放目标。

**请求**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**响应**

无。
