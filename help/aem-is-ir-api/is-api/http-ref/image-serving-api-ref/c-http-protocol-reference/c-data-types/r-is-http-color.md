---
description: 颜色值。 您可以使用十六进制记号、以逗号分隔的组件值列表或小数来指定颜色值。
seo-description: 颜色值。 您可以使用十六进制记号、以逗号分隔的组件值列表或小数来指定颜色值。
seo-title: 颜色
solution: Experience Manager
title: 颜色
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# color{#color}

颜色值。 您可以使用十六进制记号、以逗号分隔的组件值列表或小数来指定颜色值。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 颜 <span class="varname"> 色</span></span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>green<span class="varname"> , blue</span>[,rgb<span class="varname"> ,</span><span class="varname"></span>rgb]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>, magenta <span class="varname"> ,</span><span class="varname"> , black</span>yellow <span class="varname"></span>[, alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{hex6<span class="varname"> |</span>hex8<span class="varname"></span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{hex8<span class="varname"> |</span>hex10<span class="varname"></span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 红色</span>、绿 <span class="varname"> 色</span>、蓝 <span class="varname"> 色</span>、 <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>颜色组件值(0...255, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 青 <span class="varname"> 色</span>，黄色 <span class="varname"> ,</span>黑色， <span class="varname"> 洋红色，</span>Alpha <span class="varname"></span><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>CMYK颜色组件值（0.100 %，小数点） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 灰 <span class="varname"> 色</span>, <span class="varname"> alpha</span></span> </p> </td> 
  <td class="stentry"> <p>灰色分量值（0...100%，小数点） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>打包的两位十六进制灰色值(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>带有alpha颜色值(GGAA)的四位十六进制灰色 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>打包的六位十六进制RGB颜色值(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>打包的八位十六进制RGBA(RRGGBBAA)或CMYK(CCMMYYKK)颜色值（如果指定“k”后缀） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>带有alpha值的10位十六进制CMYK(CYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGB颜色的小数组件值在0...255范围内。 CMYK和灰色的小数组件值在0.100%范围内。 所有十六进制组件值都在0...0xFF范围内。

假定颜色分量值与alpha值无关（未预乘）。

所有颜色值、前缀和后缀均不区分大小写。

CMYK颜色值需要类型后缀“k”。 可以为RGB和灰色值指定类型后缀（可选）。

十六进制灰色值需要前缀&#39;0x&#39;。

“s”后缀指定颜色值与与颜色值的像素类型（定义为）对应的输入（源）色彩空间相关联 `attribute::IccProfileSrc*`。 如果不存在此后缀，则颜色值与输出（目标）色彩空间(由或定 `icc=` 义 `attribute::IccProfile*`)关联。

## 默认 {#section-737082a7da544acca8092a48d88480e7}

如果未明确指定alpha值，则假定它为255、0xFF或100%（完全不透明）。

## 示例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有效颜色说明符的一些示例及其相应的像素类型、颜色值、alpha值和默认色彩空间：

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 颜 <i>色</i></b> </th> 
   <th class="entry"> <b>像素类型</b> </th> 
   <th class="entry"> <b>颜色值</b> </th> 
   <th class="entry"> <b>Alpha值</b> </th> 
   <th class="entry"> <b>默认色彩空间 </b> </th> 
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
   <td> <p>0x010203S </p> </td> 
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
   <td> <p>100S </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
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
   <td> <p>0xddeegs </p> </td> 
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

当输出颜色的像素类型与输 `icc=` 出图像的像素类型对应时，使用应用指定的输出色彩空间代替默认色彩空间。
