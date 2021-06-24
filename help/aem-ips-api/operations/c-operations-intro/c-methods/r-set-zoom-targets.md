---
description: 设置与资产图像关联的缩放目标。 它会覆盖现有缩放目标。
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 13%

---

# setZoomTargets{#setzoomtargets}

设置与资产图像关联的缩放目标。 它会覆盖现有缩放目标。

语法

## 授权的用户类型 {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-161f8c733cc4439f94a06e12119d4226}

**Input(setZoomTargetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 包含要设置的缩放目标的资产。 |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | 是 | 缩放目标定义数组。 |

**Output(setZoomTargetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | 是 | 此操作创建的缩放目标的控制滑块集。 |

## 示例 {#section-a2f14c7a1499443e96d099ea8a76c182}

此代码示例按名称、位置（x和y轴）、宽度、高度定义一个缩放目标数组，并将该数组分配给资产。 响应包含新创建缩放目标的句柄。

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
