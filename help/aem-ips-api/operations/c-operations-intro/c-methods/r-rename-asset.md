---
description: 重命名资产。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# renameAsset{#renameasset}

重命名资产。

>[!NOTE]
>
>以前版本已弃用`renameFiles`参数，并从`renameAsset`中删除。 虚拟文件路径会进行更改以匹配新资产名称（保留文件扩展名），而物理文件路径则不会受到影响。 API客户端在更新到新API版本时，需要删除对此参数的引用。

## 授权用户类型 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读取和写入权限。

## 参数 {#section-ef95a994106841e0ab346dd4cf672258}

**输入(renameAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 资产所属公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要重命名的资产的句柄。 |
| `*`newName`*` | `xsd:string` | 是 | 资产的新名称。 |
| `*`validateName`*` | `xsd:boolean` | 是 | 如果`validateName`是`true`，并且资产类型需要唯一的IPS ID，则会检查新名称的全局唯一性，如果它不唯一，则`renameAsset`会引发故障。 |

**输出(renameAssetReturn)**

IPS API不会返回此操作的响应。 有关此元素的注意事项，请参阅`<ns1:validateName>`元素的描述。

## 示例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此代码示例可重命名资产

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
