---
title: 大小
description: 贴花大小。 贴花材质对象的宽度、高度和厚度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# 大小{#size}

贴花大小。 贴花材质对象的宽度、高度和厚度。

## 属性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

用逗号分隔的三个实数。 不得为负数。 将未使用的值设置为0。 可以省略尾随的零。

仅当应拉伸图像以适合指定的大小时，才指定宽度和高度（纵横比可能会改变）。 设置宽度或高度以按比例缩放图像。 将宽度和高度均设置为0以使用`catalog::Resolution`确定对象大小。

提供厚度值以向贴花对象添加投影。 贴花材料可选，被所有其他材料忽略。

## 默认 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0，0。 这表示要根据catalog：：Resolution确定贴花大小，并且对象没有厚度（因此不呈现投影）。

## 示例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>贴花的大小强制为12x3英寸，并且没有厚度（即没有投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5，1 </p></td> 
  <td class="stentry"> <p>贴花宽度为5英寸，高度由图像的纵横比确定，并且根据1英寸的厚度绘制投影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0，.5 </p></td> 
  <td class="stentry"> <p>贴花宽度和高度由catalog：：Resolution决定，并且厚度为1/2英寸。 </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
