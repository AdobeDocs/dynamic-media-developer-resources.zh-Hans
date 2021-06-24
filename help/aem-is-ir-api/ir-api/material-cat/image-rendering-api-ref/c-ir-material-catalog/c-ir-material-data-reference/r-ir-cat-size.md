---
description: 十进制。 倾斜材料对象的宽度、高度和厚度。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 5%

---

# 大小{#size}

十进制。 倾斜材料对象的宽度、高度和厚度。

## 属性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

三个用逗号分隔的实数。 不得为负。 将未使用的值设置为0。 可以忽略尾随零。

仅当图像应拉伸以适合指定大小时（宽高比可能会改变），才指定宽度和高度。 设置宽度或高度，以按比例缩放图像。 将宽度和高度都设置为0，以使用`catalog::Resolution`确定对象大小。

提供厚度值，以向贴图对象添加投影。 可选，适用于所有其他材料忽略的倾斜材料。

## 默认 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

一万。 这表示将根据catalog::Resolution确定十字体大小，并且对象没有厚度（因此不会渲染投影）。

## 示例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>该倾斜图被强制调整为12x3英寸大小，且无厚度（这是无投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>倾斜宽度为5英寸，高度由图像的宽高比决定，并且投影根据1英寸厚度进行渲染。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,5 </p></td> 
  <td class="stentry"> <p>倾斜宽度和高度由catalog::Resolution决定，其厚度为1/2英寸。 </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-31a164e781d14e92bd9d379d3c329e92}

[目录：:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
