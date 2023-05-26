---
description: 调整饱和度。 更改图层或复合图像的每个可见像素的饱和度。
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---

# op_saturation{#op-saturation}

调整饱和度。 更改图层或复合图像的每个可见像素的饱和度。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>饱和度调整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

`op_saturation=-100` 使图像完全去饱和。

## 属性 {#section-9a3cc9ff060049449554dfa69d92fd53}

“图层”命令。 应用于当前图层或复合图像，如果 `layer=comp`. 被效果层忽略。

## 默认 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`，表示饱和度没有变化。 在应用操作之前，CMYK图像或图层会转换为RGB。

## 示例 {#section-033b272f1b7e4efeb94e841fd8095357}

操作彩色照片以实现“高键”外观：

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
