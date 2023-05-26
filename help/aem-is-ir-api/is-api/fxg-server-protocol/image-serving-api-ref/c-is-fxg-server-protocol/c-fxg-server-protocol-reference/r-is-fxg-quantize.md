---
description: 颜色量化。 指定用于GIF输出转换的颜色量化属性。
solution: Experience Manager
title: 量化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# 量化{#quantize}

颜色量化。 指定用于GIF输出转换的颜色量化属性。

` quantize= *`type`*[, *`抖动`*[, *`numColors`*[, *`颜色列表`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 调色板类型 </p> <p>选择' <span class="codeph"> Web </span>'或' <span class="codeph"> mac </span>'以选择预定义的调色板，或设置为' <span class="codeph"> 自适应 </span>'计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抖动 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {扩散|关闭} </span> 仿色选项 </p> <p>为Floyd-Steinberg误差扩散选择“扩散”，或为“关闭”禁用仿色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>“ ”中包含的输出颜色数量（整数） <span class="codeph"> 自适应 </span>'调色板。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 必须介于2和256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色列表 </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗号分隔的强制十六进制RGB颜色列表。 允许您指定要包含在“ <span class="codeph"> 自适应 </span>'调色板。 如果指定的颜色数小于 <span class="codeph"> numColors </span>，根据图像内容计算其他颜色。 </p> <p>仅在以下情况下使用 <span class="codeph"> fmt=gif </span> 或 <span class="codeph"> fmt=gif-alpha </span>. 否则，将忽略。 指定的颜色 <span class="codeph"> <span class="varname"> 颜色列表 </span> </span> 必须为十六进制6格式的RGB值(请参阅 <span class="codeph"> 颜色 </span>)；不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“ ”生成GIF缩略图 `web`&#39;调色板无仿色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

将图像转换为具有关键色透明度的双调GIF，并强制将颜色转换为黑白色：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
