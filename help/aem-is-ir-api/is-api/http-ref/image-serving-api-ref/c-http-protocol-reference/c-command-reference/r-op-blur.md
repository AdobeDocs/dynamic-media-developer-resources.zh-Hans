---
description: 模糊图像。 将模糊滤镜应用于图像数据。
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# op_blur{#op-blur}

模糊图像。 将模糊滤镜应用于图像数据。

`op_blur= *`半径`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半径</span> </p> </td> 
  <td class="stentry"> <p>模糊滤镜半径（以像素为单位）（实数为0.100）。 </p></td> 
 </tr> 
</table>

*`radius`* 相对于复合图像的像素。还用于羽化图层效果。

## 属性 {#section-92573fe2c07746a7bab93a81fc3d208d}

层命令。 应用于当前层或复合图像（如果`layer=comp`）。

## 默认 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，不会产生模糊效果。

## 示例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊图像的背景。 `catalog::MaskPath`引用单独的蒙版图像。 请注意，必须显式指定`layer=0`，否则，会将`op_blur`应用于整个复合图像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
