---
description: 通过将资产名称与公司的图像服务/图像渲染目录命名空间的所有名称进行比较，检查IPS ID冲突。
solution: Experience Manager
title: checkassetnames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 11%

---

# checkassetnames{#checkassetnames}

通过将资产名称与公司的图像服务/图像渲染目录命名空间的所有名称进行比较，检查IPS ID冲突。

语法

## 授权用户类型 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 参数 {#section-9c75b00f2072453abea0bdefc6ad7c99}

**输入(checkAssetNamesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 包含用户的公司的句柄。 |
| assetNamesArray | `types:StringArray` | 是 | 要检查的资源名称数组。 |

**输出(checkAssetNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 是 | 正在使用的资源名称数组。 |

## 示例 {#section-bc5d120d74614a63a425ca3acc337219}

此示例代码会请求为指定公司使用的资产名称。 响应将返回一个正在使用的资源名称数组。

**请求**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**响应**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

