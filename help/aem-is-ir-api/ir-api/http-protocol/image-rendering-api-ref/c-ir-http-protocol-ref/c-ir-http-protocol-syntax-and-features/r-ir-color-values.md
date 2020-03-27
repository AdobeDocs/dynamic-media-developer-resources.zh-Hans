---
description: color=和bgc=属性的颜色值可以使用小数点、逗号分隔的组件值列表或十六进制表示法（与HTML类似）指定。
seo-description: color=和bgc=属性的颜色值可以使用小数点、逗号分隔的组件值列表或十六进制表示法（与HTML类似）指定。
seo-title: 颜色值
solution: Experience Manager
title: 颜色值
topic: Scene7 Image Serving - Image Rendering API
uuid: f8e3a8e7-3e0c-4ee6-8434-caba1f2bea1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 颜色值{#color-values}

color=和bgc=属性的颜色值可以使用小数点、逗号分隔的组件值列表或十六进制表示法（与HTML类似）指定。

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ { red, green, blue}| gray }| { [ 0x ] hex6 }| { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>红色、绿色、蓝色、灰色</i> </p></td> 
  <td class="stentry"> <p>颜色组件值（0...255，十进制整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>打包的六位十六进制RGB颜色值(RRGGBB)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>已打包两位数的十六进制灰色值(0...FF)。 </p></td> 
 </tr> 
</table>

## 示例 {#section-a78732151d584e84abeb99f9ce8d7c24}

有效颜色说明符的一些示例及其相应的RGB颜色值解释：

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
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160,177,194) </p></td> 
 </tr> 
</table>

## 另请参阅 {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [gruet=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
