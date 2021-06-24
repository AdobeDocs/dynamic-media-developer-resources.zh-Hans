---
description: 返回有关公司结构（文件数等）的信息。
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 13%

---

# getDiskUsage{#getdiskusage}

返回有关公司结构（文件数等）的信息。

## 授权用户类型 {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**输入(getDiskUsageParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要获取其磁盘使用情况的公司的句柄。 |

**输出(getDiskUsageReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | 是 | 公司磁盘使用阵列。 |

## 示例 {#section-cb16a97badc94076ad5da277db5ed16a}

此请求的名称具有误导性。 它不仅返回一个反映公司使用的磁盘空间的标量值，而是获取有关公司结构的其他信息。

**请求**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**响应**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
