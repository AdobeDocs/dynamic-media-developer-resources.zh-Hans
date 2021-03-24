---
description: 删除图像格式。 从saveImageFormat获取图像格式句柄。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# deleteImageFormat{#deleteimageformat}

删除图像格式。 从saveImageFormat获取图像格式句柄。

语法

## 授权用户类型{#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-462c05d9aad746ee8d2be0656041b693}

**Input(deleteImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要删除的图像格式的公司的句柄。 |
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 要删除的图像格式的句柄。 |

**输出(deleteImageFormatParam)**

IPS API不返回此操作的响应。

## 示例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此代码示例从公司中删除图像格式。 从其他操作获取图像格式句柄。

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
