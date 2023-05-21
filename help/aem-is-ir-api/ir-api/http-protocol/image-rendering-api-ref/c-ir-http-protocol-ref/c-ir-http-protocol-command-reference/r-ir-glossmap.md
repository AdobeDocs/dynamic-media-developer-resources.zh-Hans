---
title: glossmap
description: 光澤地圖影像。 提供可重複紋理、壁紙/邊框或貼花的光澤度的逐畫素控制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# glossmap {#glossmap}

光澤地圖影像。 提供可重複紋理、壁紙/邊框或貼花的光澤度的逐畫素控制。

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">大括弧；'是&amp;lbrace；'<span class="varname"> isReq</span>'&amp;rbrace；'&amp;rbrace；|&amp;lbrace；'&amp;lbrace；'<span class="varname"> foreignReq</span>'&amp;rbrace；' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光澤地圖影像檔案（灰階）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>影像伺服器的要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>向外部伺服器提出要求。 </p></td> 
 </tr> 
</table>

適用於金屬油漆效果、金屬箔壓切壁紙和邊框，以及金屬線織布等材料。

光澤地圖影像必須是8位元灰階，且大小與指定的主要影像相同 `src=`. 請參閱 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 以取得其他資訊。

## 屬性 {#section-26375672d69849be9b026cc93c3bc558}

材質屬性。 支援可重複的紋理、壁紙和框線以及貼花。 被純色、機櫃和視窗覆蓋材料忽略。 另請參閱 [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 以取得其他資訊。

## 默认 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

无。

## 另请参阅 {#section-33953fc1be82452da37141f2e541e00c}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)， [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
