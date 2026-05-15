---
description: 返回有关公司结构（文件数等）的信息。
solution: Experience Manager
title: getdiskusage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
TQID: 'https://experienceleague.adobe.com/mF0YHIw8BZhBRK240EmiiaHoyBbTdaW-ajl7veY1ywk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 11%

---

# getdiskusage{#getdiskusage}

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
| companyHandle | `xsd:string` | 是 | 要获取其磁盘使用情况的公司的句柄。 |

**输出(getDiskUsageReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | 是 | 公司磁盘使用数组。 |

## 示例 {#section-cb16a97badc94076ad5da277db5ed16a}

此请求的名称具有误导性。 它不会只返回反映公司正在使用的磁盘空间量的标量值，而是会获得有关公司结构的其他信息。

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
