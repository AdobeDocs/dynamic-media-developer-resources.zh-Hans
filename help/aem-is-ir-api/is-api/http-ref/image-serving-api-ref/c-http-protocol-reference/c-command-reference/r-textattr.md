---
description: 文本层属性。 为无法用作rtf命令的文本层指定其他属性。
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# textAttr{#textattr}

文本层属性。 为无法用作rtf命令的文本层指定其他属性。

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>提供了一种在不更改字体大小的情况下缩放文本图层的方法。 分辨率值越高，呈现的文本相对于画布大小的大小就越大；值越小，文本大小就越小。 文本分辨率（以每英寸点为单位）（整数大于0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 抗锯齿  </span> </span> </p> </td> 
  <td class="stentry"> <p>控制文本渲染引擎采用的消除锯齿模式。 </p> <p> <span class="codeph"> 关闭 |范数 |清晰 |锐 | strong |平滑  </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
      <td class="stentry"> <p>禁用文本消除锯齿。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 规范  </span> </p> </td> 
      <td class="stentry"> <p>启用标准文本消除锯齿模式（默认）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 脆脆  </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph">清晰的</span>（仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 锐  </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph">锐化</span>（仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 强 </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph"> strong </span>（仅限<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制在渲染文本时如何使用分辨率 </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率。 </p> <p>如果文本要以相对于合成画布的精确大小呈现，则使用。 如果文本框太小，文本可以剪切到图层大小（如果指定）。 这是<span class="codeph"> textPs= </span>支持的唯一<span class="varname"> resMode </span>选项。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>自动调整分辨率，以最好地用文本直接填充图层。 </p> <p>使用可自动调整文本大小，以便尽可能地填充文本框，而不会出现截断的风险。 如果启用了自动换行，则文本可能会以最终分辨率重新换行。 <span class="varname"> 如果 </span> 选择autoRes ，则 <span class="codeph"> 会 </span> 忽略res。<span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率；根据需要减小，以防止文本被截断为层直接。 </p> <p>只要未发生剪切，就使用以精确指定的分辨率渲染文本。 剪切时，分辨率会自动降低，以确保所有文本都完全包含在文本框内。 如果启用了自动换行，则文本可能会以最终分辨率重新换行。 <span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未使用size=指定文本层大小，或者如果仅指定宽度，则将忽略“autoRes”和“maxRes”设置，并使用指定的分辨率来渲染文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定封装模式。 </p> <p> <span class="codeph"> 包装 | noWrap | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>禁用自动换行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 换行 </span> </p> </td> 
      <td class="stentry"> <p>启用标准自动换行。 </p> <p>如有必要，可中断长词。 <span class="codeph"> textPs=仅 </span> 支持 <span class="codeph"> 换 </span>行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>启用不中断的自动换行。 </p> <p>一个字就算在结尾被截断，也不会中断。 通常与<span class="codeph"> autoRes </span>或<span class="codeph"> maxRes </span>一起使用，以确保长词永远不会断开。 </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph">在单词边界和连字符上自动换行</span>和<span class="codeph">在单词边界和连字符上自动换行</span>。 </p> </td> 
 </tr> 
</table>

## 属性 {#section-114ca0b8585b403c873e2251478ad1d5}

文本层属性。 被图像、纯色和效果图层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。

## 默认 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另请参阅 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
