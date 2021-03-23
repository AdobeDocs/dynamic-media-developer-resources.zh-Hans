---
description: 颜色量化。 指定GIF输出转换的颜色量化属性。
seo-description: 颜色量化。 指定GIF输出转换的颜色量化属性。
seo-title: 数量
solution: Experience Manager
title: 数量
uuid: 624cdc45-51f2-4b18-a658-311770974521
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 数量化{#quantize}

颜色量化。 指定GIF输出转换的颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 类型  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}调 </span> 板类型 </p> <p>选择“<span class="codeph"> web </span>”或“<span class="codeph"> mac </span>”以选择预定义的调色板，或设置为“<span class="codeph"> adaptive </span>”以计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dusfer|off}仿 </span> 色选项 </p> <p>为Floyd-Steinberg错误扩散选择“扩散”或“关”以禁用仿色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>“ <span class="codeph"> adaptive </span>”调板中包含的输出颜色（整数）数。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 必须介于2和256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗号分隔的列表十六进制6格式的强制RGB颜色。 允许您指定要包含在“ <span class="codeph"> adaptive </span>”调板中的强制颜色。 如果指定的颜色数小于<span class="codeph"> numColors </span>，则根据图像内容计算其他颜色。 </p> <p>仅在<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>时使用。 否则忽略。 使用<span class="codeph"> <span class="varname"> colorList </span> </span>指定的颜色必须是十六进制6格式的RGB值（请参阅<span class="codeph"> color </span>）；不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“ `web`”调板生成GIF缩览图，无仿色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

将图像转换为具有键控颜色透明度的双色调GIF，并将颜色强制为黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
