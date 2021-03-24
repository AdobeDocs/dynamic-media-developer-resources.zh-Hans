---
description: 设置资产的图像映射。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

设置资产的图像映射。

您必须已创建图像映射。 根据从数组检索的顺序应用图像映射。 这意味着第二个图像映射叠加第一个图像映射，第三个图像映射叠加第二个图像映射，依此类推。

## 授权用户类型{#section-adb21c5b679249939dd83816e4a0ee97}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | 是 | 预定义图像映射的数组。 |

**输出(setImageMapsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | 是 | 具有应用于资产的图像映射手柄的数组。 |

## 示例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此代码示例为图像资产设置2个图像映射。 该代码指定调用图像映射时采取的形状类型、区域和操作。 响应包含一个数组，其中包含对图像映射的句柄。

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

