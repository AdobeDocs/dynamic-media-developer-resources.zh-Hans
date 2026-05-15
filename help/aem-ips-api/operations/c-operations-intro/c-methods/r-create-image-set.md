---
description: 创建图像集。
solution: Experience Manager
title: createImageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
TQID: 'https://experienceleague.adobe.com/os4DfkGa5cTZfMN1vc5HeA8Qvauvwb5Q0dZ2P3HFI-c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 13%

---

# createImageset{#createimageset}

创建图像集。

语法

## 授权用户类型 {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对目标文件夹的读/写访问权限。

## 参数 {#section-03d22ba7d290477e91c25ca1d4439200}

**输入(createImageSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 图像集所属公司的句柄。 |
| folderHandle | `xsd:string` | 是 | 文件夹的句柄。 |
| 名称 | `xsd:string` | 是 | 图像集名称。 |
| 类型 | `xsd:string` | 是 | 图像集类型。 |
| thumbAssetHandle | `xsd:string` | 否 | 充当新图像集缩略图的资产句柄。 如果未指定，则IPS会尝试使用集合引用的第一个图像资产。 |

**输出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 新图像集的句柄。 |

## 示例 {#section-385fe3b0af8044b0a2451336ec137fc5}

此代码示例创建一个由公司、文件夹、名称和类型指定的图像集。 响应是新创建图像集的资产句柄。

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
