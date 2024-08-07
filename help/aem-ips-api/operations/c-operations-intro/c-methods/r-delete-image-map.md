---
description: 删除图像映射。
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---

# deleteImageMap{#deleteimagemap}

删除图像映射。

语法

## 授权用户类型 {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写访问权限。

## 参数 {#section-28de12bab79045a5977c68855e37ae3d}

**输入(deleteImageMapParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要删除的图像映射的公司的句柄。 |
| imageMapHandle | `xsd:string` | 是 | 要删除的图像映射的句柄。 |

**输出(deleteImageMapParam)**

IPS API不返回此操作的响应。

## 示例 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

此代码示例从公司中删除图像映射。 必须从另一个操作获取图像映射句柄。

**请求**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**响应**

无
