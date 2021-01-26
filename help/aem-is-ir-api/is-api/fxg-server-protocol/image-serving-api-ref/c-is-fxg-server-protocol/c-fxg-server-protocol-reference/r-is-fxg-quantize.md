---
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-title: 量化
solution: Experience Manager
title: 量化
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 数量化{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 类型  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}调色板 </span> 类型 </p> <p>选择“ <span class="codeph"> web </span>”或“ <span class="codeph"> mac </span>”以选择预定义的调色板，或设置为“ <span class="codeph"> adaptive </span>”以计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {扩散|关)仿 </span> 色选项 </p> <p>为Floyd-Steinberg错误扩散选择“扩散”或“关闭”以禁用仿色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>“ <span class="codeph"> adaptive </span>”调色板中包含的输出颜色（整数）数。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 必须介于2和256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>以十六进制6格式的强制RGB颜色的逗号分隔列表。 允许您指定要包含在“ <span class="codeph"> adaptive </span>”调色板中的强制颜色。 如果指定的颜色数小于<span class="codeph"> numColors </span>，则根据图像内容计算其他颜色。 </p> <p>仅当<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>时使用。 否则忽略。 使用<span class="codeph"> <span class="varname"> colorList </span> </span>指定的颜色必须是十六进制格式的RGB值（请参阅<span class="codeph">颜色</span>）;不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“ `web`”调色板生成GIF缩略图，无仿色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

将图像转换为具有键色透明度的双色调GIF，并强制颜色转换为黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
