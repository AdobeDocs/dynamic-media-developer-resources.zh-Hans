---
title: 檢視屬性
description: 這些指令與位置無關，而且可能出現在請求中的任何位置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 18e1ee40-fe34-435a-be97-849b08618d48
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# 檢視屬性{#view-attributes}

這些指令與位置無關，而且可能出現在請求中的任何位置。

<table id="simpletable_D30C7420AECD44ADBD7B0728594FF5FA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt</a> </span> </p></td> 
  <td class="stentry"> <p>回覆影像格式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt</a> </span> </p></td> 
  <td class="stentry"> <p>JPEG品質。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-printres.md#reference-ff897ad013fb410b96edaa2c79edfddd" type="reference" format="dita" scope="local"> printRes</a> </span> </p></td> 
  <td class="stentry"> <p>列印內嵌在回覆影像中的解析度值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478" type="reference" format="dita" scope="local"> hei</a></span> </p></td> 
  <td class="stentry"> <p>將演算後的影像縮放至指定的高度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec" type="reference" format="dita" scope="local"> wid</a></span> </p></td> 
  <td class="stentry"> <p>將演算後的影像縮放至指定的寬度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29" type="reference" format="dita" scope="local"> scl</a></span> </p></td> 
  <td class="stentry"> <p>相對於完整解析度的暈映大小縮放演算後的影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3" type="reference" format="dita" scope="local"> resMode</a></span> </p></td> 
  <td class="stentry"> <p>重新取樣模式以進行最終影像縮放。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e" type="reference" format="dita" scope="local"> 銳利化</a></span> </p></td> 
  <td class="stentry"> <p>回覆影像銳利化。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc</a></span> </p></td> 
  <td class="stentry"> <p>輸出色彩設定檔。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed</a></span> </p></td> 
  <td class="stentry"> <p>將色彩設定檔內嵌在回覆影像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed</a></span> </p></td> 
  <td class="stentry"> <p>在回覆影像中內嵌Photoshop路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-vignette.md#reference-eb3f458733294f988483b024348bc778" type="reference" format="dita" scope="local"> 暈映</a></span> </p></td> 
  <td class="stentry"> <p>晕影. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-cache.md#reference-a83329ce7c914ee4b518b0bda71f0438" type="reference" format="dita" scope="local"> 快取</a></span> </p> </td> 
  <td class="stentry"> <p>覆寫預設的回應快取行為。 </p></td> 
 </tr> 
</table>
