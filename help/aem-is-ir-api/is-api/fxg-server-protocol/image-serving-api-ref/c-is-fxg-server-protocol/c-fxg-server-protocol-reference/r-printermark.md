---
description: 显示打印机标记。 指定如何显示打印机标记。
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 30%

---


# printerMark{#printermark}

显示打印机标记。 指定如何显示打印机标记。

` printerMark= *`裁切标`*, *`记出`*, *`血标记注`*, *`册标`*, *`记颜`*, *``*, *`色条`*, *`页信息线粗细图层嵌入`*`

可以关闭或打开不同的标记。 还可以控制打印机标记的样式。

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
  <td class="stentry"> <p>默认为默认 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>行权重= </p></td> 
  <td class="stentry"> <p>范围0.125 - 2.0中的任意值（包括这两个值）。 </p></td> 
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
