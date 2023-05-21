---
title: 範例A
description: 使用靜態背景影像建立固定大小的範本，此可變影像在左中心與背景對齊，並縮放至不超過背景寬度與高度的80%。 最後，在畫布的右邊緣置中對齊垂直文字的文字圖層。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 範例A{#example-a}

使用靜態背景影像建立固定大小的範本，此可變影像在左中心與背景對齊，並縮放至不超過背景寬度與高度的80%。 最後，在畫布的右邊緣置中對齊垂直文字的文字圖層。

![範例影像](assets/examplea.png)

## 範本記錄 {#section-32f54710593e438fa0622224c89380af}

插入物件

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog：：Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog：：Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text+goes+here&amp;text=rtf.....rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0 </span> </p> </td> 
 </tr> 
</table>

此 `origin=` 所有圖層的值在範本中明確指定，以嚴格控制圖層的定位和對齊。 每個圖層原點都會設定為符合該圖層的所需對齊方式。 此 `origin=` 背景的（圖層0）設定為中心；此值是任意的，因為背景影像在執行階段不會變更；可以使用圖層0原點的任何值。

此 `pos=` 值會在圖層原點之間提供所需的位移，以達到所需的圖層定位。

圖層1影像的錨點會放置在左中央，並透過 `pos=` 值。 此設定可達成背景與第1層影像之間的左中對齊，無論第1層影像的外觀比例為何。

同樣地，文字圖層的錨點位於自動調整大小的文字方塊的中央，且 `pos=` 值。 此設定可達成所需旋轉文字的右中對齊，不受字型大小和字串長度影響。

實際顯示文字是在執行階段提供，所以會使用變數將文字與rtf格式設定信封分開。 預設變數 `$object` 用於第1層影像。 此變數可讓您在請求路徑中指定此影像。

任何影像都可用於背景影像和圖層1影像。 如果背景影像有遮色片，則未遮色片區域會以預設背景顏色( `attribute::BkgColor`)，或保持透明，當 `fmt=png-alpha` 或 `fmt=tif-alpha`. 如果背景影像具有非正方形的外觀比例，它會在回覆影像中置中，而額外的空間會填滿 `attribute::BkgColor`. 如果圖層1影像有Alpha資料或遮色片，背景影像（或背景顏色）在透明區域中仍保持可見。 如果影像沒有遮色片，則會填滿整個配置的矩形。

## 使用範本 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示圖層1影像的不同外觀比例和不同文字字串的複合結果。

![範例複合結果影像](assets/exampleausing.png)
