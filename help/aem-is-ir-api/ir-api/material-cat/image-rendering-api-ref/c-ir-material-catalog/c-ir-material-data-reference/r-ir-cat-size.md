---
description: 戴尔大小。 倾斜材料对象的宽度、高度和厚度。
seo-description: 戴尔大小。 倾斜材料对象的宽度、高度和厚度。
seo-title: 大小
solution: Experience Manager
title: 大小
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 5%

---


# 大小{#size}

戴尔大小。 倾斜材料对象的宽度、高度和厚度。

## 属性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

三个用逗号分隔的实数。 不得为负。 将未使用的值设置为0。 可省略尾随零。

仅当图像应拉伸以适合指定大小时（长宽比可能会更改），才指定宽度和高度。 设置宽度或高度，以按比例缩放图像。 将宽度和高度都设置为0，以使用`catalog::Resolution`确定对象大小。

提供厚度值，以向贴花对象添加投影。 对于倾斜材料是可选的，被所有其他材料忽略。

## 默认 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

万，万。 这表示将根据catalog::Resolution确定贴花大小，并且该对象没有厚度（因此不会呈现投影）。

## 示例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>贴花板的大小被强制为12x3英寸，并且没有厚度（即，没有投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>倾斜宽度为5英寸，高度由图像的长宽比决定，投影根据1英寸厚度进行渲染。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>倾斜宽度和高度由catalog::Resolution决定，为半英寸厚。 </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
