---
description: 确定一批资产是否准备好发布。
seo-description: 确定一批资产是否准备好发布。
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Dynamic Media Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

确定一批资产是否准备好发布。

这是[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)的批处理版本。

## 授权用户类型{#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

## 参数 {#section-3e49d7859f8647b990d75373cc8dbc24}

**输入(setAssetsPublishStateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | 是 | 资产的发布状态值的数组。 |

**输出(setAssetsPublishStateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新的资产数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试更新时生成警告的资产数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试删除时生成错误的资产数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产更新关联的详细信息，这些更新生成了警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与生成错误的资产更新关联的详细信息。 |

## 示例 {#section-38cfdd3436214a06a1bae16875501d51}

此代码示例设置资产的发布状态。

**请求**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**响应**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

