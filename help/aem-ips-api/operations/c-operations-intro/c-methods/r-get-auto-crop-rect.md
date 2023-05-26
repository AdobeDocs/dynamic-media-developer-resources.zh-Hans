---
description: 根据图像的背景颜色或透明度返回图像的裁剪区域。
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 15%

---

# getAutoCropRect{#getautocroprect}

根据图像的背景颜色或透明度返回图像的裁剪区域。

语法

## 授权用户类型 {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

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
>调用此方法时，请指定autoColorCropOptions或autoTransparentCropOptions。

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有您要使用的资产的公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 要处理的资源的句柄。 |
| autoColorCropOptions | `types:AutoColorCropOptions` | 否 | 根据颜色计算裁切矩形。 参见 [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | 否 | 根据透明度计算裁切矩形。 参见 [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**输出(getAutoCropRectReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| xOffset | `xsd:int` | 是 | 计算裁切区域的起始左像素坐标。 |
| y偏移 | `xsd:int` | 是 | 计算裁切区域的起始顶部像素坐标。 |
| 宽度 | `xsd:int` | 是 | 计算裁剪区域的宽度（以像素为单位）。 |
| 高度 | `xsd:int` | 是 | 计算裁剪区域的高度（以像素为单位）。 |

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

