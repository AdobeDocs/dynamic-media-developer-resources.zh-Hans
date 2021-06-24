---
description: 确定是否已准备好发布一批资产。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# setAssetsPublishState{#setassetspublishstate}

确定是否已准备好发布一批资产。

这是[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)的批处理版本。

## 授权用户类型 {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读取和写入权限。

## 参数 {#section-3e49d7859f8647b990d75373cc8dbc24}

**输入(setAssetsPublishStateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | 是 | 资产的发布状态值数组。 |

**输出(setAssetsPublishStateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更新资产的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试更新时生成警告的资产数量。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试删除时生成错误的资产数量。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与生成警告的资产更新关联的详细信息。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与生成错误的资产更新关联的详细信息。 |

## 示例 {#section-38cfdd3436214a06a1bae16875501d51}

此代码示例可设置资产的发布状态。

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
