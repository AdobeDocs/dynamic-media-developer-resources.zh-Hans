---
description: 设置与资产图像关联的缩放目标。 它覆盖现有缩放目标。
seo-description: 设置与资产图像关联的缩放目标。 它覆盖现有缩放目标。
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Dynamic Media Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 12%

---


# setZoomTargets{#setzoomtargets}

设置与资产图像关联的缩放目标。 它覆盖现有缩放目标。

语法

## 已授权的用户类型{#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-161f8c733cc4439f94a06e12119d4226}

**输入(setZoomTargetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 具有要设置的缩放目标的资产。 |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | 是 | 缩放目标定义的数组。 |

**输出(setZoomTargetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | 是 | 此操作创建的缩放目标的手柄集。 |

## 示例 {#section-a2f14c7a1499443e96d099ea8a76c182}

此代码示例按名称、位置（x和y轴）、宽度、高度定义一组缩放目标，并将该数组分配给资产。 响应包含对新创建的缩放目标的句柄。

**请求**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**响应**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```

