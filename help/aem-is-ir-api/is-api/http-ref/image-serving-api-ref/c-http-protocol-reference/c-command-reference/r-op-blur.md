---
description: 模糊图像。 对图像数据应用模糊滤镜。
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# op_blur{#op-blur}

模糊图像。 对图像数据应用模糊滤镜。

`op_blur= *`半径`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半径</span> </p> </td> 
  <td class="stentry"> <p>模糊滤镜半径（以像素为单位）（实数0.100）。 </p></td> 
 </tr> 
</table>

*`radius`* 以像素为单位，相对于合成图像。还用于羽化图层效果。

## 属性 {#section-92573fe2c07746a7bab93a81fc3d208d}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，以消除模糊效果。

## 示例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊图像的背景。 单独的蒙版图像由`catalog::MaskPath`引用。 请注意，必须显式指定`layer=0`，否则`op_blur`将应用于整个复合图像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
