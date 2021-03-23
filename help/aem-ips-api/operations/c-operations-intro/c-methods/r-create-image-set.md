---
description: 创建图像集。
seo-description: 创建图像集。
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 14%

---


# createImageSet{#createimageset}

创建图像集。

语法

## 授权用户类型{#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有目标文件夹的读/写访问权限。

## 参数 {#section-03d22ba7d290477e91c25ca1d4439200}

**Input(createImageSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 图像集所属公司的手柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 文件夹的句柄。 |
| `*`name`*` | `xsd:string` | 是 | 图像集名称。 |
| `*`类型`*` | `xsd:string` | 是 | 图像集类型。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 用作新图像集缩略图的资产处理。 如果未指定，IPS将尝试使用由集引用的第一个图像资源。 |

**输出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 新图像集的手柄。 |

## 示例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此代码示例创建由公司、文件夹、名称和类型指定的图像集。 响应是新创建的图像集的资产句柄。

**请求**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**响应**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```

