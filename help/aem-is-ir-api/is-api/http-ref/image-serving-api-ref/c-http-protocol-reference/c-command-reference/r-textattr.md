---
description: 文字圖層屬性。 指定無法做為rtf指令的文字圖層其他屬性。
solution: Experience Manager
title: textAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c8a3d2a-2524-436a-8bc7-60241af0fd17
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 1%

---

# textAttr{#textattr}

文字圖層屬性。 指定無法做為rtf指令的文字圖層其他屬性。

` textAttr= *`res`*[, *`消除鋸齒`*[, *`解析模式`*[, *`自動換行`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span> </span> </p> </td> 
  <td class="stentry"> <p>提供縮放文字圖層而不變更字型大小的方法。 較高的解析度值會增加相對於畫布大小的演算文字大小；較小的值會減少文字大小。 以每英吋點數為單位的文字解析度（整數大於0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 消除鋸齒 </span> </span> </p> </td> 
  <td class="stentry"> <p>控制文字轉譯引擎所使用的消除鋸齒模式。 </p> <p> <span class="codeph"> 關閉 |標準 |清爽 |銳利化 |強 |平滑 </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
      <td class="stentry"> <p>停用文字消除鋸齒。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 標準 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準文字消除鋸齒模式（預設）。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 清晰 </span> </p> </td> 
      <td class="stentry"> <p>選取Photoshop消除鋸齒模式 <span class="codeph"> 清晰 </span> ( <span class="codeph"> textPs= </span> 僅限)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 銳利化 </span> </p> </td> 
      <td class="stentry"> <p>選取Photoshop消除鋸齒模式 <span class="codeph"> 銳利化 </span> ( <span class="codeph"> textPs= </span> 僅限)。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 強 </span> </p> </td> 
      <td class="stentry"> <p>選取Photoshop消除鋸齒模式 <span class="codeph"> 強 </span> ( <span class="codeph"> textPs= </span> 僅限)。 </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span> </span> </p> </td> 
  <td class="stentry"> <p>控制呈現文字時如何使用res </p> <p> <span class="codeph"> fixedRes | autoRes | maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度。 </p> <p>如果要以相對於合成畫布的確切大小呈現文字，請使用。 如果文字方塊太小，可以將文字裁剪成圖層大小（如果已指定）。 這是唯一 <span class="varname"> 解析模式 </span> 支援的選項 <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>自動調整解析度，讓文字以最佳方式填滿圖層矩形。 </p> <p>使用可自動調整文字大小，讓文字方塊儘可能填滿，不會有截斷的風險。 如果已啟用自動換行，文字可能會以最終解析度重新換行。 <span class="varname"> res </span> 被忽略，如果 <span class="codeph"> autoRes </span> 「 」已選取。 不支援 <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>使用指定的解析度；如有必要，請減少此解析度，以防止文字被截斷到圖層矩形。 </p> <p>只要沒有剪裁發生，使用以完全指定的解析度呈現文字。 若是剪裁，解析度會自動降低，以確保所有文字都完全包含在文字方塊內。 如果已啟用自動換行，文字可能會以最終解析度重新換行。 不支援 <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>如果未以size=指定文字圖層大小或僅指定寬度，則會忽略'autoRes'和'maxRes'設定，並使用指定的解析度來轉譯文字。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 自動換行 </span> </span> </p> </td> 
  <td class="stentry"> <p>指定換行模式。 </p> <p> <span class="codeph"> 換行 | noWrap | nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>停用自動換行。 </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> 换行 </span> </p> </td> 
      <td class="stentry"> <p>啟用標準自動換行。 </p> <p>如有必要，請換長字。 <span class="codeph"> textPs= </span> 僅支援 <span class="codeph"> 換行 </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>啟用不間斷的換行。 </p> <p>一個字詞絕不中斷，即使它在結尾被截斷。 通常搭配使用 <span class="codeph"> autoRes </span> 或 <span class="codeph"> maxRes </span> 以確保長字不會中斷。 </p> </td> 
     </tr> 
    </table> </p> <p>兩者 <span class="codeph"> 換行 </span> 和 <span class="codeph"> nbwrap </span> 自動繞排文字邊界和連字型大小。 </p> </td> 
 </tr> 
</table>

## 屬性 {#section-114ca0b8585b403c873e2251478ad1d5}

文字圖層屬性。 被影像、純色和效果圖層忽略。 套用至 `layer=0` 若指定給 `layer=comp`.

## 默认 {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## 另请参阅 {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) ， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)， [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
