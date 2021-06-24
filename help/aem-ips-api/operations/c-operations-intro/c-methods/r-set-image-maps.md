---
description: 设置资产的图像映射。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

设置资产的图像映射。

您必须已创建图像映射。 按照从数组中检索的顺序应用图像映射。 这表示第二个图像映射叠加了第一个图像映射，第三个图像映射叠加了第二个图像映射，依此类推。

## 授权用户类型 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2292ec1aead947ef8741dd0653a41f42}

**Input(setImageMapsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | 是 | 预定义图像映射的数组。 |

**输出(setImageMapsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | 是 | 一个数组，其中图像映射句柄应用于资产。 |

## 示例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此代码示例为图像资产设置了2个图像映射。 该代码指定在调用图像映射时采取的形状类型、区域和操作。 响应包含一个带有图像映射句柄的数组。

**请求**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```
