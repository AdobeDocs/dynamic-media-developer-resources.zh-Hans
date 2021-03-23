---
description: 文本图层属性。 指定不能用作rtf命令的文本图层的其他属性。
seo-description: 文本图层属性。 指定不能用作rtf命令的文本图层的其他属性。
seo-title: textAttr
solution: Experience Manager
title: textAttr
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 1%

---


# textAttr{#textattr}

文本图层属性。 指定不能用作rtf命令的文本图层的其他属性。

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res  </span> </span> </p> </td> 
  <td class="stentry"> <p>提供一种在不更改字体大小的情况下缩放文本图层的方法。 分辨率值越高，渲染的文本相对于画布大小越大；值越小，文本大小就越小。 文本分辨率（以每英寸点数为单位）（整数大于0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> antiAliasing  </span> </span> </p> </td> 
  <td class="stentry"> <p>控制文本渲染引擎采用的消除锯齿模式。 </p> <p> <span class="codeph"> 关闭 |规范 |清晰 |锐化 | strong |平滑  </span> </p> <p> 
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
      <td class="stentry"> <p> <span class="codeph"> 脆  </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph">（仅限<span class="codeph"> textPs= </span>）。</span> </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 锐  </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph"> sharp </span>（仅<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 强 </span> </p> </td> 
      <td class="stentry"> <p>选择Photoshop消除锯齿模式<span class="codeph"> strong </span>（仅<span class="codeph"> textPs= </span>）。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制渲染文本时如何使用分辨率 </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes  </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率。 </p> <p>如果要以与合成画布相对的精确大小渲染文本，则使用。 如果文本框太小，文本可能会被剪切到图层大小（如果指定）。 这是<span class="codeph"> textPs= </span>支持的唯一<span class="varname"> resMode </span>选项。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes  </span> </p> </td> 
      <td class="stentry"> <p>自动调整分辨率，使用文本填充图层矩形。 </p> <p>使用可自动调整文本大小，以便尽可能填充文本框，而不会出现截断风险。 如果启用了换行，则文本可以在最终分辨率重新换行。 <span class="varname"> 如果 </span> 选择了“自动 <span class="codeph"> 重 </span> 新显示”，则忽略res。<span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes  </span> </p> </td> 
      <td class="stentry"> <p>使用指定的分辨率；如果需要，请减少该值，以防止文本被截断到图层矩形。 </p> <p>只要不发生剪切，就可以使用以精确指定的分辨率渲染文本。 在剪切的情况下，分辨率会自动降低，以确保所有文本都完全包含在文本框中。 如果启用了换行，则文本可以在最终分辨率重新换行。 <span class="codeph"> textPs= </span>不支持。 </p> </td> 
     </tr> 
    </table> </p> <p>如果未指定size=的文本图层大小，或仅指定宽度，则忽略“autoRes”和“maxRes”设置，并使用指定分辨率来渲染文本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定打包模式。 </p> <p> <span class="codeph"> 绕 |无绕排 | nbWrap  </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap  </span> </p> </td> 
      <td class="stentry"> <p>禁用自动换行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 换行 </span> </p> </td> 
      <td class="stentry"> <p>启用标准换行。 </p> <p>如有必要，可以换掉长词。 <span class="codeph"> textPs=仅 </span> 支持 <span class="codeph"> 绕 </span>排。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap  </span> </p> </td> 
      <td class="stentry"> <p>启用不间断的换行。 </p> <p>一个词永远不要断开，即使它在结尾被截断。 通常与<span class="codeph"> autoRes </span>或<span class="codeph"> maxRes </span>一起使用，以确保长词永不中断。 </p> </td> 
     </tr> 
    </table> </p> <p><span class="codeph">在字边界和连字符上自动换行</span>和<span class="codeph">。</span> </p> </td> 
 </tr> 
</table>

## 属性 {#section-114ca0b8585b403c873e2251478ad1d5}

文本图层属性。 被图像、纯色和效果图层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。

## 默认 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另请参阅 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
