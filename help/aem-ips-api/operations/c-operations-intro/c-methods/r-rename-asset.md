---
description: 重命名资源。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
TQID: 'https://experienceleague.adobe.com/m1AT0yP7u3PFZCs8uoFQxQoGNtfJe49vzGt8e3wTx8s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 6%

---

# renameAsset{#renameasset}

重命名资源。

>[!NOTE]
>
>`renameFiles`参数在以前的版本中已弃用，已从`renameAsset`中删除。 虚拟文件路径将更改以匹配新的资源名称（保留文件扩展名），而物理文件路径不受影响。 在更新到新的API版本时，API客户端需要移除对此参数的引用。

## 授权用户类型 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写访问权限。

## 参数 {#section-ef95a994106841e0ab346dd4cf672258}

**输入(renameAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 资产所属公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 要重命名的资源的句柄。 |
| newName | `xsd:string` | 是 | 资产的新名称。 |
| validateName | `xsd:boolean` | 是 | 如果`validateName`为`true`，并且资产类型需要唯一的IPS ID，则会检查新名称是否具有全局唯一性，如果`renameAsset`不是唯一名称，则会引发错误。 |

**输出(renameAssetReturn)**

IPS API不返回此操作的响应。 有关此元素的注意事项，请参阅`<ns1:validateName>`元素的描述。

## 示例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此代码示例用于重命名资源

**请求**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**响应**

无。
