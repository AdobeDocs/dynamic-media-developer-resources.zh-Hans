---
title: 颜色值
description: color=和bgc=属性的颜色值可以使用小数、逗号分隔的组件值列表或十六进制表示法来指定，类似于HTML。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# 颜色值{#color-values}

可以使用十进制、逗号分隔的组件值列表或十六进制表示法(类似于HTML)来指定`color=`和`bgc=`属性的颜色值。

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">颜色</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {红色，绿色，蓝色} | 灰色} | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>红色，绿色，蓝色，灰色</i> </p></td> 
  <td class="stentry"> <p>颜色组件值（0至255，十进制整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>十六进制6</i> </p></td> 
  <td class="stentry"> <p>打包了六位十六进制RGB色值(RRGGBB)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>已打包两位数的十六进制灰度值(0...FF)。 </p></td> 
 </tr> 
</table>

## 示例 {#section-a78732151d584e84abeb99f9ce8d7c24}

有效颜色说明符及其相应RGB颜色值解释的一些示例：

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,100,200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128,128,128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2，3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160,177,194) </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)，[bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0)，[grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
