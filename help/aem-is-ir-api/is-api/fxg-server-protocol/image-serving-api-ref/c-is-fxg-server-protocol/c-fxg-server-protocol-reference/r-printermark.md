---
description: 显示打印机标记。 指定如何显示打印机标记。
solution: Experience Manager
title: 打印机标记
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
TQID: 'https://experienceleague.adobe.com/tit-a3stXGj0fZoMgi15lPIk-MtZSvUDOqlcayfNlwk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 24%

---

# 打印机标记{#printermark}

显示打印机标记。 指定如何显示打印机标记。

` printerMark= *`修剪标记`*, *`出血标记`*, *`注册标记`*, *`颜色条`*, *`页面信息`*, *`样式`*, *`线宽`*, *`图层嵌入`*`

可以关闭或打开不同的标记。 也可以控制打印机标记的样式。

以下是有效值：

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>修剪标记= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>流血痕迹= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>注册标记= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>颜色条= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>页面信息= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为 0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>默认 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>默认为“默认” </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>线条粗细= </p></td> 
  <td class="stentry"> <p>0.125 - 2.0范围内的任何值，包括这两个值。 </p></td> 
  <td class="stentry"> <p>默认值为0.25。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>图层嵌入= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>默认值为1。 </p></td> 
 </tr> 
</table>

## 示例 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
