---
description: 倾斜大小。 倾斜材质对象的宽度、高度和厚度。
seo-description: 倾斜大小。 倾斜材质对象的宽度、高度和厚度。
seo-title: 大小
solution: Experience Manager
title: 大小
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 5%

---


# 大小{#size}

倾斜大小。 倾斜材质对象的宽度、高度和厚度。

## 属性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

用逗号隔开的三个实数。 不得为负。 将未使用的值设置为0。 可省略尾随零。

仅当图像应拉伸以适合指定大小时（长宽比可能会更改），才指定宽度和高度。 设置宽度或高度以按比例缩放图像。 将宽度和高度都设置为0以使用`catalog::Resolution`确定对象大小。

提供厚度值，以向贴花对象添加投影。 对于倾斜材料是可选的，被所有其他材料忽略。

## 默认 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

一万。 这表示将根据catalog::Resolution确定贴花大小，并且对象没有厚度（因此不会渲染投影）。

## 示例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>贴花板的尺寸强制为12x3英寸，无厚度（即无投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>倾斜宽度为5英寸，高度由图像的长宽比决定，投影根据1英寸厚度绘制。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>倾斜宽度和高度由catalog::Resolution决定，并且是1/2英寸厚。 </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
