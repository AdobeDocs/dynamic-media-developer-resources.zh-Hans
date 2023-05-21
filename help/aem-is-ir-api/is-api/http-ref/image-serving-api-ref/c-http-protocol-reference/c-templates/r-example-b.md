---
description: 與範例A的需求類似，但使用純色背景，並允許複合物高度改變，以容納不同外觀比例的影像。
solution: Experience Manager
title: 範例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# 範例B{#example-b}

與範例A的需求類似，但使用純色背景，並允許複合物高度改變，以容納不同外觀比例的影像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

影像置入圖層0中，高度值為 `size=` 設為0。 此設定會讓實際高度由影像縮放至800畫素寬後的高度決定。

變數 `extend=` 在頂端和底部增加100畫素，在右側增加200畫素。

圖層0和圖層1的原點都放在合成區域的右中角，以取得所要的文字位置。

下圖顯示不同影像外觀比例和不同文字字串的複合結果。

![範例B影像](assets/exampleb.png)
