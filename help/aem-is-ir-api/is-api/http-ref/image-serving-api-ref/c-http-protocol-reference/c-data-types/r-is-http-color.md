---
description: 颜色值。 您可以使用十六进制表示法、以逗号分隔的组件值列表或小数位数指定颜色值。
solution: Experience Manager
title: 颜色
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
TQID: 'https://experienceleague.adobe.com/3NfMrvwXTP9A-KoxjVPtps-0rhO5xNd04WUlrdCQEo8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 9%

---

# 颜色{#color}

颜色值。 您可以使用十六进制表示法、以逗号分隔的组件值列表或小数位数指定颜色值。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">颜色</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;lcub；&amp;lcub；<span class="varname"> gray</span>[，<span class="varname"> alpha</span>][g]&amp;rcub；|</span> </p> <p> <span class="codeph"> {<span class="varname">红色</span>，<span class="varname">绿色</span>，<span class="varname">蓝色</span>[ ，<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname">青色</span>，<span class="varname">洋红色</span>，<span class="varname">黄色</span>，<span class="varname">黑色</span>[，alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname">十六进制6</span>|<span class="varname">十六进制8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname">十六进制8</span>|<span class="varname">十六进制10</span>}k}&amp;rcub；[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">红色</span>，<span class="varname">绿色</span>，<span class="varname">蓝色</span>，<span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>颜色组件值（0到255，十进制整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">青色</span>，<span class="varname">洋红色</span>，<span class="varname">黄色</span>，<span class="varname">黑色</span>，<span class="varname">阿尔法</span></span> </p></td> 
  <td class="stentry"> <p>CMYK颜色组件值（0..100 %，十进制整数） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">灰色</span>，<span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>灰度分量值（0至100%，十进制整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六进制2</span> </span> </p></td> 
  <td class="stentry"> <p>压缩的两位十六进制灰色颜色值(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六进制4</span> </span> </p> </td> 
  <td class="stentry"> <p>用Alpha颜色值填充四位十六进制灰度(GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六进制6</span> </span> </p> </td> 
  <td class="stentry"> <p>打包的6位十六进制RGB颜色值(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六进制8</span> </span> </p> </td> 
  <td class="stentry"> <p>打包了八位十六进制RGBA (RRGGBBAA)或CMYK (CCMMYKK)颜色值（如果以“k”后缀指定） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">十六进制10</span> </span> </p></td> 
  <td class="stentry"> <p>带alpha值的十位十六进制CMYK (CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGB颜色的小数组件值在0至255之间。 CMYK和灰度的小数组件值在0..100%范围内。 所有十六进制组件值在0到0之间的范围内。

假定颜色分量值与alpha值无关（不是预乘）。

所有颜色值、前缀和后缀均不区分大小写。

CMYK颜色值需要类型后缀“k”。 可以选择为RGB和灰色值指定类型后缀。

十六进制灰度值需要前缀“0x”。

“s”后缀指定颜色值与对应于颜色值的像素类型（使用`attribute::IccProfileSrc*`定义）的输入（源）色彩空间相关联。 如果此后缀不存在，则颜色值与输出（目标）颜色空间（使用`icc=`或`attribute::IccProfile*`定义）关联。

## 默认 {#section-737082a7da544acca8092a48d88480e7}

如果未明确指定alpha值，则假定为255、0xFF或100%（完全不透明）。

## 示例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有效颜色说明符及其相应像素类型、颜色值、Alpha值和默认颜色空间的一些示例：

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>颜色</i> </b> </th> 
   <th class="entry"> <b>像素类型</b> </th> 
   <th class="entry"> <b>颜色值</b> </th> 
   <th class="entry"> <b>Alpha值</b> </th> 
   <th class="entry"> <b>默认色彩空间</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203秒 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100秒 </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75克 </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddegs </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

当输出颜色的像素类型对应于输出图像的像素类型时，将应用通过`icc=`指定的输出颜色空间而不是默认颜色空间。
