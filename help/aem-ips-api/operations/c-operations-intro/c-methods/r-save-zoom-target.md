---
description: 创建或编辑缩放目标。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 20%

---

# saveZoomTarget{#savezoomtarget}

创建或编辑缩放目标。

语法

## 授权用户类型 {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4a23983cae4e49a098e9bbe736933996}

**输入(saveZoomTargetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要保存的缩放目标的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 缩放目标的手柄。 |
| `*`zoomTargetHandle`*` | `xsd:string` | 否 | 编辑或创建缩放目标。 |
| `*`name`*` | `xsd:string` | 是 | 缩放目标名称。 |
| `*`xPosition`*` | `xsd:int` | 是 | 左像素位置。 |
| `*`yPosition`*` | `xsd:int` | 是 | 顶部像素位置。 |
| `*`width`*` | `xsd:int` | 是 | 缩放目标宽度。 |
| `*`height`*` | `xsd:int` | 是 | 缩放目标高度。 |
| `*`用户数据`*` | `xsd:string` | 是 | 以了解客户特定的信息。 可以包含任何类型的数据。 |

**输出(saveZoomTargetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | 是 | 处理新创建的缩放目标。 |

## 示例 {#section-509c472c316549cdb228d7e1cfa8400a}

此代码示例保存缩放目标。 响应会返回缩放目标句柄。

**请求**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**响应**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
