---
description: 创建或编辑缩放目标。
seo-description: 创建或编辑缩放目标。
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 19%

---


# saveZoomTarget{#savezoomtarget}

创建或编辑缩放目标。

语法

## 授权用户类型{#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4a23983cae4e49a098e9bbe736933996}

**Input(saveZoomTargetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 带有要保存的缩放目标的公司的手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 缩放目标的手柄。 |
| `*`zoomTargetHandle`*` | `xsd:string` | 否 | 编辑或创建缩放目标。 |
| `*`name`*` | `xsd:string` | 是 | 缩放目标名称。 |
| `*`xPosition`*` | `xsd:int` | 是 | 左像素位置。 |
| `*`yPosition`*` | `xsd:int` | 是 | 顶部像素位置。 |
| `*`width`*` | `xsd:int` | 是 | 缩放目标宽度。 |
| `*`height`*` | `xsd:int` | 是 | 缩放目标高度。 |
| `*`用户数据`*` | `xsd:string` | 是 | 有关客户特定信息。 可以包含任何类型的数据。 |

**输出(saveZoomTargetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | 是 | 处理新创建的缩放目标。 |

## 示例 {#section-509c472c316549cdb228d7e1cfa8400a}

此代码示例保存缩放目标。 响应返回缩放目标手柄。

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

