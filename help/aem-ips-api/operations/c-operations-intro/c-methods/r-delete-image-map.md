---
description: 删除图像映射。
seo-description: 删除图像映射。
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---


# deleteImageMap{#deleteimagemap}

删除图像映射。

语法

## 授权用户类型{#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

## 参数 {#section-28de12bab79045a5977c68855e37ae3d}

**输入(deleteImageMapParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含要删除的图像映射的公司的句柄。 |
| ` *`imageMapHandle`*` | `xsd:string` | 是 | 要删除的图像映射的句柄。 |

**输出(deleteImageMapParam)**

IPS API不返回此操作的响应。

## 示例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此代码范例将从公司中删除图像映射。 必须从其他操作获取图像映射句柄。

**请求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**响应**

无
