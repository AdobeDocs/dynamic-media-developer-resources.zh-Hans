---
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
solution: Experience Manager
title: 数量
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# 数量{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}调 </span> 板类型 </p> <p>选择“ <span class="codeph"> web </span>”或“ <span class="codeph"> mac </span>”以选择预定义调色板，或将设置为“ <span class="codeph">自适应</span>”以计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dusfer|off}抖动选 </span> 项 </p> <p>为Floyd-Steinberg误差扩散选择“扩散”或“关闭”以禁用抖动。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>“ <span class="codeph">自适应</span>”调色板中包含的输出颜色数（整数）。 </p> <p> <span class="codeph"> <span class="varname"> numColors必 </span> </span> 须介于2到256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗号分隔的十六进制6格式强制RGB颜色列表。 用于指定要包含在“ <span class="codeph">自适应</span>”调色板中的强制颜色。 如果指定的颜色数小于<span class="codeph"> numColors </span>，则会根据图像内容计算其他颜色。 </p> <p>仅当<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>时使用。 否则，将忽略。 使用<span class="codeph"> <span class="varname"> colorList </span> </span>指定的颜色必须是十六进制格式的RGB值（请参阅<span class="codeph">颜色</span>）；不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“ `web`”面板生成GIF缩略图，且无抖动：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

将图像转换为具有键色透明度的双色调GIF，并强制将颜色转换为黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
