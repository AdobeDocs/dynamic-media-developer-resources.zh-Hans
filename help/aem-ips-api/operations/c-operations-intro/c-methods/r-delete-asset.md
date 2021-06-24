---
description: 删除资产。
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

---

# deleteAsset{#deleteasset}

删除资产。

语法

## 授权用户类型 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读取和删除权限。

## 参数 {#section-0eed164e278b456fbdfb7a50727a0416}

**输入(deleteAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 文件夹所属的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要删除的资产的句柄。 |

**输出(deleteAssetParam)**

IPS API不会返回此操作的响应。

## 示例 {#section-d5657289f5234bb0a613dcf691507958}

此示例代码会从特定公司删除任何类型的资产。 它需要一个资产句柄，您必须从其他操作中获取该句柄。

**请求**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**响应**

无。
