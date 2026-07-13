---
description: 设置资源的图像映射。
solution: Experience Manager
title: setImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
TQID: 'https://experienceleague.adobe.com/sOGDO0ruTEK1DS5Sc-4nhLfViddEKCLDLJlpC-8H3g0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 134
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

