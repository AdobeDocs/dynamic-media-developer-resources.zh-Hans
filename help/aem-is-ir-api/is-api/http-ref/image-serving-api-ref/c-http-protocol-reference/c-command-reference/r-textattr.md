---
title: textAttr
description: 文本图层属性。 为文本图层指定其他属性，这些属性不能作为rtf命令使用。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# textAttr{#textattr}

文本图层属性。 为文本图层指定其他属性，这些属性不能作为rtf命令使用。

` textAttr= *`res`*[, *`antiAliasing`*[, *`resMode`*[, *`wordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">资源</span> </span> </p> </td> 
  <td class="stentry"> <p>它提供了一种缩放文本图层而不更改字体大小的方法。 分辨率值越高，呈现的文本相对于画布大小大小越大；值越小，文本大小越小。 文本分辨率，以每英寸点数（整数大于0）为单位。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">消除锯齿</span> </span> </p> </td> 
  <td class="stentry"> <p>控制文本渲染引擎使用的消除锯齿模式。 </p> <p> <span class="codeph">关 | 范数 | 清晰 | 锐化 | 强 | 平滑</span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">折扣</span> </p> </td> 
      <td class="stentry"> <p>禁用文本消除锯齿。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">标准</span> </p> </td> 
      <td class="stentry"> <p>启用标准文本消除锯齿模式（默认）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">清晰</span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph">清晰的</span> （仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">锐化</span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph">锐化</span> （仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">强</span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph"> strong </span> （仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制呈现文本时使用res的方式 </p> <p> <span class="codeph">个固定资源 | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率。 </p> <p>如果文本要以相对于合成画布的确切大小呈现，则使用。 如果文本框太小，可以将文本裁剪为图层大小（如果已指定）。 这是<span class="varname"> textPs= </span>唯一支持的<span class="codeph"> resMode </span>选项。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">自动确定</span> </p> </td> 
      <td class="stentry"> <p>自动调整分辨率以用文本最好地填充图层矩形。 </p> <p>使用可自动调整文本大小，以便尽可能多地填充文本框，而不会截断风险。 如果启用了自动换行，则文本可能会以最终分辨率重新换行。 如果选择<span class="varname">自动确定</span>，则会忽略<span class="codeph">确定</span>。 <span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率；如有必要，请减小该分辨率，以防止文本被截断到图层矩形。 </p> <p>使用以指定的分辨率呈现文本，只要不进行剪切即可。 如果进行了剪切，则分辨率会自动降低，以确保所有文本都完全包含在文本框中。 如果启用了自动换行，则文本可能会以最终分辨率重新换行。 <span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未使用size=或仅指定宽度来指定文本图层大小，则会忽略“autoRes”和“maxRes”设置。 在这种情况下，使用指定的分辨率来呈现文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">自动换行</span> </span> </p> </td> 
  <td class="stentry"> <p>指定封装模式。 </p> <p> <span class="codeph">换行 | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>禁用自动换行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph">自动换行</span> </p> </td> 
      <td class="stentry"> <p>启用标准自动换行。 </p> <p>如果必要的话，它会断掉长语。 <span class="codeph"> textPs= </span>仅支持<span class="codeph">换行</span>。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>启用不间断自动换行。 </p> <p>从不断字，即使它在结尾被截断。 通常与<span class="codeph"> autoRes </span>或<span class="codeph"> maxRes </span>一起使用，以确保不会损坏长单词。 </p> </td> 
     </tr> 
    </table> </p> <p>在单词边界和连字符上，<span class="codeph">自动换行</span>和<span class="codeph">自动换行</span>。 </p> </td> 
 </tr> 
</table>

## 属性 {#section-114ca0b8585b403c873e2251478ad1d5}

文本图层属性。 被图像、纯色和效果图层忽略。 如果为`layer=0`指定，则应用于`layer=comp`。

## 默认 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另请参阅 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ，[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)，[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
