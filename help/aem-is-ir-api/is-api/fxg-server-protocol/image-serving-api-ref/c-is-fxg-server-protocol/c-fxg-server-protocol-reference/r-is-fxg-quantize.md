---
title: 量化
description: 颜色量化。 指定GIF输出转换的颜色量化属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# 量化{#quantize}

颜色量化。 指定GIF输出转换的颜色量化属性。

` quantize= *`类型`*[, *`递色`*[, *`numColors`*[, *`颜色列表`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">类型</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span>调色板类型 </p> <p>选择“<span class="codeph"> web </span>”或“<span class="codeph"> mac </span>”以选择预定义的调色板，或设置为“<span class="codeph">自适应</span>”以计算图像的最佳调色板。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">仿色</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {扩散|关闭} </span>个仿色选项 </p> <p>为Floyd-Steinberg误差扩散选择“扩散”，或为“关闭”禁用仿色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>“<span class="codeph">最合适</span>”调色板中包含的输出颜色数量（整数）。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span>必须介于2到256之间。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">颜色列表</span> </span> </p> </td> 
  <td class="stentry"> <p>以逗号分隔的强制十六进制RGB颜色列表。 允许您指定要包含在“<span class="codeph">最合适</span>”调色板中的强制颜色。 如果指定的颜色数小于<span class="codeph"> numColors </span>，则根据图像内容计算其他颜色。 </p> <p>仅在<span class="codeph"> fmt=gif </span>或<span class="codeph"> fmt=gif-alpha </span>时使用。 否则，将忽略。 使用<span class="codeph"> <span class="varname"> colorList </span> </span>指定的颜色必须是十六进制格式的RGB值（请参阅<span class="codeph">颜色</span>）；不允许使用其他颜色说明符。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用“`web`”调色板生成GIF缩略图且无仿色：

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

将图像转换为具有关键颜色透明度的双调GIF并强制将颜色转换为黑白：

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
