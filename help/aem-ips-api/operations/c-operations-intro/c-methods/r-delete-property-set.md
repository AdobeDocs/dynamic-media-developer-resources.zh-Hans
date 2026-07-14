---
description: 删除属性集和所有相关属性。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
TQID: 'https://experienceleague.adobe.com/1j45J5Kw5P-3ba3WLNy9sTDBC5g4L17bynJQRaU5lAM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 10%

---

# deletePropertySet{#deletepropertyset}

删除属性集和所有相关属性。

语法

## 授权用户类型 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e5fc868f69494cf6858e03027db09101}

**输入(deletePropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 要删除的属性集的句柄。 |

**输出(deletePropertySetParam)**

IPS API不返回此操作的响应。

## 示例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此代码示例将该集的句柄用作发送到IPS Web服务服务器的`deletePropertySetParam`中的字段以删除属性集。

**请求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**响应**

无。

