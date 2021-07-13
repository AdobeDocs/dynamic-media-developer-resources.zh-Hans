---
description: 显示打印机标记。 指定如何显示打印机标记。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 31%

---

# printerMark{#printermark}

显示打印机标记。 指定如何显示打印机标记。

` printerMark= *`裁切`*, *`标记`*, *`标记注`*, *`册标记颜`*, *`色标`*, *``*, *`记信息`*, *`样式线粗细层嵌入`*`

可以关闭或打开不同的标记。 打印机标记的样式也可以控制。

以下是有效值：

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
  <td class="stentry"> <p>默认为 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>线重量= </p></td> 
  <td class="stentry"> <p>范围为0.125 - 2.0的任何值，包括这两个值。 </p></td> 
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
