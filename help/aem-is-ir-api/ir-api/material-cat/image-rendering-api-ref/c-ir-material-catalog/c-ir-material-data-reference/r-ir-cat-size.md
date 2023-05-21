---
description: 貼花大小。 貼花材質物件的寬度、高度和厚度。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 4%

---

# 大小{#size}

貼花大小。 貼花材質物件的寬度、高度和厚度。

## 屬性 {#section-967bf1112eec4032a91ed0c8a7b10a07}

以逗號分隔的三個實數。 不得為負數。 將未使用的值設為0。 可省略結尾的零。

只有在影像應拉伸以符合指定大小時，才指定寬度和高度（外觀比例可能會變更）。 設定寬度或高度以按比例縮放影像。 將寬度和高度都設定為0以使用 `catalog::Resolution`以決定物件大小。

提供厚度值，以將投影增加到貼花物件。 貼花材質的選擇性，被其他所有材質忽略。

## 默认 {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. 這表示要根據catalog：：Resolution來決定貼花大小，而且物件沒有厚度（因此不會呈現投影）。

## 示例 {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>貼花的尺寸強製為12x3英吋，且沒有厚度（這表示沒有投影）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>貼花寬度為5英吋，高度由影像的外觀比例決定，而投影會根據1英吋的厚度彩現。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>貼花寬度和高度由catalog：：Resolution決定，且厚度為1/2英吋。 </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-31a164e781d14e92bd9d379d3c329e92}

[catalog：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
