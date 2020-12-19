---
description: 删除资产。
seo-description: 删除资产。
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
topic: Scene7 Image Production System API
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 12%

---


# deleteAsset{#deleteasset}

删除资产。

语法

## 授权用户类型{#section-e913be43b684491daf02bc73211e4290}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 文件夹所属公司的句柄。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 要删除的资产的句柄。 |

**输出(deleteAssetParam)**

IPS API不返回此操作的响应。

## 示例 {#section-d5657289f5234bb0a613dcf691507958}

此示例代码从特定公司删除任何类型的资产。 它需要一个资产句柄，您必须从其他操作获取该句柄。

**请求**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**响应**

无。
