---
description: 删除图像格式。 从saveImageFormat获取图像格式句柄。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 11%

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

**Input(deleteImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要删除的图像格式的公司句柄。 |
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 要删除的图像格式的句柄。 |

**输出(deleteImageFormatParam)**

IPS API不会返回此操作的响应。

## 示例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此代码示例会从公司中删除图像格式。 从其他操作中获取图像格式句柄。

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
