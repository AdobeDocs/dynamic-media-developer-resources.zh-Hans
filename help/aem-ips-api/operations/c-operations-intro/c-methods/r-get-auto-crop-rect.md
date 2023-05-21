---
description: 根據影像的背景顏色或透明度，傳回影像的裁切區域。
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

根據影像的背景顏色或透明度，傳回影像的裁切區域。

语法

## 授權的使用者型別 {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**輸入(getAutoCropRectParam)**

>[!NOTE]
>
>呼叫此方法時，請指定autoColorCropOptions或autoTransparentCropOptions。

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 擁有您要使用之資產的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 您要使用之資產的控點。 |
| autoColorCropOptions | `types:AutoColorCropOptions` | 否 | 根據顏色計算裁切矩形。 另請參閱 [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | 否 | 根據透明度計算裁切矩形。 另請參閱 [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**輸出(getAutoCropRectReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| xOffset | `xsd:int` | 是 | 計算裁切區域的起始左側畫素座標。 |
| yOffset | `xsd:int` | 是 | 計算裁切區域的起始頂端畫素座標。 |
| 宽度 | `xsd:int` | 是 | 計算裁切區域的寬度（畫素）。 |
| 高度 | `xsd:int` | 是 | 計算裁切區域的高度（畫素）。 |

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

