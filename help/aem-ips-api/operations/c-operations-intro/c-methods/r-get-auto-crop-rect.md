---
description: 根据图像的背景颜色或透明度为图像返回裁剪区域。
seo-description: 根据图像的背景颜色或透明度为图像返回裁剪区域。
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Dynamic Media Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 13%

---


# getAutoCropRect{#getautocroprect}

根据图像的背景颜色或透明度为图像返回裁剪区域。

语法

## 授权用户类型{#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**输入(getAutoCropRectParam)**

>[!NOTE]
>
>在调用此方法时，指定`*`autoColorCropOptions`*`或`*`autoTransparentCropOptions`*`。

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要处理的资产的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要处理的资产的句柄。 |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | 否 | 根据颜色计算裁剪矩形。 请参阅[ AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)。 |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | 否 | 根据透明度计算裁剪矩形。 请参阅[AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)。 |

**输出(getAutoCropRectReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | 是 | 计算的裁剪区域的起始左像素坐标。 |
| `*`yOffset`*` | `xsd:int` | 是 | 计算的裁剪区域的起始顶部像素坐标。 |
| `*`width`*` | `xsd:int` | 是 | 计算的裁剪区域的宽度（以像素为单位）。 |
| `*`height`*` | `xsd:int` | 是 | 计算的裁剪区域的高度（以像素为单位）。 |

## 示例 {#section-ba65bd66086d491cad1cea535954ee1f}

**请求**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**响应**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

