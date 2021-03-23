---
description: 重命名资产。
seo-description: 重命名资产。
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 6%

---


# renameAsset{#renameasset}

重命名资产。

>[!NOTE]
>
>`renameFiles`参数已在先前版本中弃用，并已从`renameAsset`中删除。 虚拟文件路径将更改为与新资源名称（保留文件扩展名）匹配，而物理文件路径不受影响。 API客户端在更新到新API版本时需要删除对此参数的引用。

## 授权用户类型{#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

## 参数 {#section-ef95a994106841e0ab346dd4cf672258}

**Input(renameAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 资产所属公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要重命名的资产的句柄。 |
| `*`newName`*` | `xsd:string` | 是 | 资产的新名称。 |
| `*`validateName`*` | `xsd:boolean` | 是 | 如果`validateName`为`true`，且资源类型需要唯一的IPS ID，则会检查新名称的全局唯一性，如果它不唯一，则`renameAsset`将引发错误。 |

**输出(renameAssetReturn)**

IPS API不返回此操作的响应。 有关此元素的注意事项，请参见`<ns1:validateName>`元素的说明。

## 示例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

此代码示例重命名资产

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
