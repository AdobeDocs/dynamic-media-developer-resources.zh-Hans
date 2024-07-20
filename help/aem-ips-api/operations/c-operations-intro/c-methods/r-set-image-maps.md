---
description: 设置资源的图像映射。
solution: Experience Manager
title: setImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 10%

---

# setImageMap{#setimagemaps}

设置资源的图像映射。

您必须已创建图像映射。 图像映射按从阵列中检索的顺序应用。 这意味着第二图像映射叠加第一图像映射，第三图像映射叠加第二图像映射，依此类推。

## 授权用户类型 {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2292ec1aead947ef8741dd0653a41f42}

**输入(setImageMapsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| assetHandle | `xsd:string` | 是 | 资产句柄。 |
| imageMapArray | `types:ImageMapDefinitionArray` | 是 | 预定义图像映射的数组。 |

**输出(setImageMapsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | 是 | 一个数组，其中包含应用于资源的图像映射句柄。 |

## 示例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

此代码示例为一个图像资源设置2个图像映射。 该代码指定调用图像映射时执行的形状类型、区域和操作。 响应包含一个数组，其中包含图像映射的句柄。

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
