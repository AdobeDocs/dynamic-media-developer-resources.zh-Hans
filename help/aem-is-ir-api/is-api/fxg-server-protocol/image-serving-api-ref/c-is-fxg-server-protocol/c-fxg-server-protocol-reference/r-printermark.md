---
description: 顯示印表機標籤。 指定如何顯示印表機標籤。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 33%

---

# printerMark{#printermark}

顯示印表機標籤。 指定如何顯示印表機標籤。

` printerMark= *`修剪標籤`*, *`出血標籤`*, *`註冊標籤`*, *`色條`*, *`頁面資訊`*, *`樣式`*, *`線條寬度`*, *`圖層內嵌`*`

可以關閉或開啟不同的標籤。 也可以控制印表機標籤的樣式。

以下是有效的值：

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>默认 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>預設為預設 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>線條寬度= </p></td> 
  <td class="stentry"> <p>介於0.125到2.0之間的任何值，包括這兩個值。 </p></td> 
  <td class="stentry"> <p>默认值为 0.25。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 1。 </p></td> 
 </tr> 
</table>

## 示例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
