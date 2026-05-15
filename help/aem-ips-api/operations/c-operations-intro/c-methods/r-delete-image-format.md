---
description: 删除图像格式。 从saveImageFormat获取图像格式句柄。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
TQID: 'https://experienceleague.adobe.com/BOhXqXdUG6BUA9VsI9faDIeRfdCwlqYsj6sqS-uQ330'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 9%

---

# deleteImageFormat{#deleteimageformat}

删除图像格式。 从saveImageFormat获取图像格式句柄。

语法

## 授权用户类型 {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-462c05d9aad746ee8d2be0656041b693}

**输入(deleteImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要删除的图像格式的公司句柄。 |
| imageFormatHandle | `xsd:string` | 是 | 要删除的图像格式的句柄。 |

**输出(deleteImageFormatParam)**

IPS API不返回此操作的响应。

## 示例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此代码示例从公司中删除图像格式。 从另一个操作获取图像格式句柄。

**请求**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**响应**

无。

**相关主题：**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
