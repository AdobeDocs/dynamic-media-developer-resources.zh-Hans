---
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-title: 量化
solution: Experience Manager
title: 量化
topic: Scene7 Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 量化{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *`TypedithernumColorscolorList`*[, *``*[, *``*[, *``*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 类型 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac}调色板类 </span> 型 </p> <p>选择“ <span class="codeph"> web </span>”或“ <span class="codeph"> mac”以选择预定义的调色板，或设置为“ </span>adaptive <span class="codeph"></span>”以计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖动 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {dumsal|off}仿色 </span> 选项 </p> <p>为Floyd-Steinberg错误扩散选择“扩散”或“关闭”可禁用仿色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色数 </span></span> </p> </td> 
  <td class="stentry"> <p>“自适应”调色板中包含的输出颜色( <span class="codeph"> 整 </span>数)数。 </p> <p> <span class="codeph"> num <span class="varname"> Colors </span> 必 </span> 须介于2和256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 颜 <span class="varname"> 色列表 </span></span> </p> </td> 
  <td class="stentry"> <p>以十六进制6格式的强制RGB颜色列表，以逗号分隔。 允许您指定要包含在“自适应”调色板中 <span class="codeph"> 的强 </span>制颜色。 如果指定的颜色数小于numColors <span class="codeph"> ，则 </span>会根据图像内容计算其他颜色。 </p> <p>仅在fmt=gif或fmt <span class="codeph"></span> =gif-alpha时使用 <span class="codeph"></span>。 否则忽略。 使用colorList指定的 <span class="codeph"> 颜 <span class="varname"> 色 </span> 必须是十六进制6格式的RGB值(请参 </span> 阅颜 <span class="codeph"></span>色);不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“”调板生成GIF缩 `web`览图，无仿色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

将图像转换为具有主色透明度的双色调GIF，并将颜色强制为黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
