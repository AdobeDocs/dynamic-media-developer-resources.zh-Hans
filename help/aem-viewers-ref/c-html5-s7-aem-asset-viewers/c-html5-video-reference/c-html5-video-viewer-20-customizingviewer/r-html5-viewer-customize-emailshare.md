---
title: 電子郵件共用
description: 電子郵件共用工具包含新增至「社交」共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1788e069-68dd-4960-bc49-34ffdf29991a
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '2987'
ht-degree: 2%

---

# 電子郵件共用{#email-share}

電子郵件共用工具包含新增至「社交」共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

電子郵件共用按鈕的外觀由以下CSS類別選取器控制：

```
.s7videoviewer .s7emailshare
```

**電子郵件共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

您可以透過設定從「社交分享」面板移除按鈕 `display:none` CSS屬性的CSS類別。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 設定28 x 28畫素的電子郵件共用按鈕，並為四種不同按鈕狀態分別顯示不同影像。

```
.s7videoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7videoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7videoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7videoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

使用下列CSS類別選取器可控制對話方塊啟動時覆蓋網頁的背景覆蓋：

```
.s7videoviewer .s7emaildialog .s7backoverlay
```

**背面覆蓋的CSS屬性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> 背景覆蓋不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將背景覆蓋設定為具有70%不透明度的灰色：

```
.s7videoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

依預設，強制回應對話方塊會以案頭系統熒幕的中心顯示，並會使用觸控裝置上的整個網頁區域。 在所有情況下，對話方塊的位置和大小都由元件管理。 此對話方塊由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialog
```

**對話方塊的CSS屬性**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 對話方塊邊框半徑（如果對話方塊未取用整個瀏覽器視窗）； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 對話方塊背景顏色； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 應取消設定或設為100%，此時對話方塊會取用整個瀏覽器視窗（觸控裝置偏好此模式）； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 應取消設定或設為100%，此時對話方塊會取用整個瀏覽器視窗（觸控裝置偏好此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定對話方塊以使用整個瀏覽器視窗並在觸控裝置上擁有白色背景：

```
.s7videoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

對話方塊標頭包含圖示、標題文字和關閉按鈕。 標題容器由下列CSS類別選擇器控制

```
.s7videoviewer .s7emaildialog .s7dialogheader
```

**對話方塊標頭的CSS屬性**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 標頭內容的內部內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

圖示和標題文字會包裝進由控制的額外容器中

```
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**對話方塊行的CSS屬性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 標頭圖示和標題的內邊距 </p> </td> 
  </tr> 
 </tbody> 
</table>

頁首圖示由下列CSS類別選擇器控制

```
.s7videoviewer .s7emaildialog .s7dialogheadericon
```

**對話方塊標頭圖示的CSS屬性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>圖示高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>圖示影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

標題標題由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogheadertext
```

**對話方塊標頭文字的CSS屬性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字型高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內部文字內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用下列CSS類別選取器來控制「關閉」按鈕：

```
.s7videoviewer .s7emaildialog .s7closebutton
```

**關閉按鈕的CSS屬性**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 相對於頁首容器的垂直按鈕位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 相對於頁首容器的水準按鈕位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>按鈕的內部內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

「關閉」按鈕工具提示和對話方塊標題可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要設定含邊框間距的對話方塊標頭，請選取24 x 17畫素圖示、粗體16點標題和28 x 28畫素關閉按鈕。 最後，請將其放置在上方兩個畫素，以及對話方塊容器右側兩個畫素：

```
.s7videoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話方塊頁尾包含「取消」和「傳送電子郵件」按鈕。 頁尾容器由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogfooter
```

**對話方塊頁尾**的CSS屬性

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 可用來從視覺上分隔頁尾與對話方塊其餘部分的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

頁尾有保留兩個按鈕的內部容器。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**對話方塊按鈕容器的CSS屬性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 頁尾和按鈕之間的內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

取消按鈕由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogcancelbutton
```

**對話方塊取消按鈕的CSS屬性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

傳送電子郵件按鈕由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogactionbutton
```

**對話方塊動作按鈕的CSS屬性**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 每個狀態的按鈕背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

此外，這兩個按鈕共用共用的CSS類別可以包含與其他對話方塊按鈕相同的CSS設定：

```
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button
```

**按鈕的CSS屬性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> 按鈕內的文字高度。 影響垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>陰影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右邊界 </span> </p> </td> 
   <td colname="col2"> <p>右按鈕邊界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要設定具有64 x 34 「取消」按鈕和82 x 34 「傳送電子郵件」按鈕的對話方塊頁尾，且每個按鈕狀態的文字顏色和背景顏色不同：

```
.s7videoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主要對話方塊區域（在頁首和頁尾之間）右側包含可捲動對話方塊內容和捲動面板。 在任何情況下，元件都會管理此區域的寬度，無法在CSS中加以設定。 主要對話方塊區域由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogviewarea
```

對話方塊檢視區域的**CSS屬性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 主要對話方塊區域的高度。 只有在對話方塊在案頭模式中運作時，才應指定它。 當對話方塊的大小設定為佔據整個瀏覽器視窗時，此選項不適用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>主要對話方塊區域的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外部邊界。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>主要對話方塊區域支援選用的 `state` 屬性選擇器。 它設定為 `sendsuccess` 當電子郵件表單提交且對話方塊顯示確認訊息時。 只要確認訊息很小，就可以使用此屬性選取器來減少顯示此類確認訊息時對話方塊的高度。

範例 — 若要將主要對話方塊區域設定為最初為300畫素高度，而在顯示確認訊息時為100畫素高度，請有10畫素邊界，並使用白色背景：

```
.s7videoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7videoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

所有表單內容（例如標籤和輸入欄位）都位在容器內，由控制

```
.s7videoviewer .s7emaildialog .s7dialogbody
```

如果此容器的高度看起來大於主對話方塊區域，元件會自動啟用垂直捲動。

對話方塊主體**的**CSS屬性

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定表單內容為十畫素邊框間距：

```
.s7videoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

對話方塊表單是逐行填入，其中每一行都包含部分表單內容（如標籤和文字輸入欄位）。 單一表單行由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**對話方塊行的CSS屬性**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內線邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定對話方塊表單，讓每行有10個畫素內距：

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

對話方塊表單中的所有靜態標籤都由控制

```
.s7videoviewer .s7emaildialog .s7dialoglabel
```

此類別不適合控制標籤大小或位置，因為您可以將其套用至表單使用者介面不同位置的文字。

對話方塊標籤的**CSS屬性。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>標簽字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>標簽字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>標簽字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>標籤文字色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

對話方塊標籤可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 將所有標籤設定為灰色、粗體加九畫素字型：

```
.s7videoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

所有顯示在表單輸入欄位左側的靜態標籤皆由下列專案控制：

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel
```

**對話方塊輸入標籤的CSS屬性**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>靜態標籤內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將輸入欄位標籤設定為50畫素寬度，請靠右對齊、有10個畫素的內距，並在右側有10個畫素邊界：

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

每個表單輸入欄位都會包裝在容器中，讓您在輸入欄位周圍套用自訂邊框。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer
```

**對話方塊輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位容器周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>輸入欄位容器支援選擇性 `state` 屬性選擇器。 它設定為 `verifyerror` 當使用者在輸入資料格式中錯誤且內嵌驗證失敗時。 此屬性選擇器可用來反白顯示表單中錯誤的使用者輸入。

從標籤展開至對話方塊內文左邊緣到右邊緣的大部分輸入欄位（包括「寄件者」欄位和「訊息」欄位）都是透過下列方式控制：

```
.s7videoviewer .s7emaildialog .s7dialoginputwide
```

**對話方塊輸入範圍欄位的CSS屬性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「收件者」輸入欄位較窄，因為它會為右側的「移除電子郵件」按鈕分配空間。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialoginputshort
```

**對話方塊的CSS屬性輸入短欄位**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定表單使其有一個畫素灰色邊框，且所有輸入欄位周圍有九個畫素的內距。 對於驗證失敗的欄位，要有相同的紅色邊框，要有250畫素寬的「至」輸入欄位，其餘輸入欄位有300畫素寬：

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

電子郵件訊息輸入欄位也由以下控制：

```
.s7videoviewer .s7emaildialog .s7dialogmessage
```

此類別可讓您設定基礎專案的特定屬性 `TEXTAREA` 元素。

**對話方塊訊息的CSS屬性**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>訊息高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動換行 </span> </p> </td> 
   <td colname="col2"> <p>文字環繞樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將電子郵件訊息設定為高50畫素並使用 `break-word` 自動換行：

```
.s7videoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

「新增其他電子郵件地址」按鈕可讓使用者在電子郵件表單中新增多個收件者。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton
```

**對話方塊的CSS屬性新增電子郵件地址按鈕**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>按鈕區域內部的按鈕影像位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>按鈕字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>按鈕內的文字高度。 影響垂直對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要將「新增其他電子郵件地址」按鈕設定為25畫素高，請使用對齊方式正確的12點粗體字型，並針對每個狀態使用不同的文字顏色和影像：

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

「移除」按鈕可讓使用者從電子郵件表單中移除額外的收件者。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**對話方塊的CSS屬性移除電子郵件按鈕**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要將「移除」按鈕設定為25 x 25畫素，並為每個狀態使用不同的影像：

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

共用的內容會顯示在對話方塊內文底部，並包含縮圖、標題、來源URL和說明。 它會包裝在容器中，並受到下列控制：

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

對話方塊內容的**CSS屬性**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>容器邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定底部容器，使其有一個畫素虛線框線且沒有邊框間距：

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

使用下列CSS類別選取器可控制縮圖影像：

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail
```

此 `background-image` 屬性是由元件邏輯所設定。

**對話方塊縮圖影像的CSS屬性**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>垂直對齊縮圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將縮圖設定為90 x 60畫素，並且以10個畫素的內距對齊：

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

內容標題、來源和說明會進一步分組到內容縮圖右側的面板中。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel
```

**對話方塊資訊面板的CSS屬性**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>面板寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將內容資訊面板設定為300畫素寬：

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

內容標題由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogtitle
```

**對話方塊標題的CSS屬性**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外部邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定內容標題以使用粗體字型並有10畫素邊界：

```
.s7videoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

內容來源由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogorigin
```

對話方塊內容來源**的**CSS屬性

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外部邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定內容來源為10畫素邊界：

```
.s7videoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

內容說明由下列CSS類別選擇器控制：

```
.s7videoviewer .s7emaildialog .s7dialogdescription
```

**對話方塊內容說明的CSS屬性**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外部邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定具有十畫素邊界的內容說明，並使用九點字型：

```
.s7videoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

當使用者輸入不正確的輸入資料且內嵌驗證失敗時，或者在提交表單時對話方塊必須呈現錯誤或確認訊息時，對話方塊內文的頂部會顯示訊息。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage
```

**對話方塊的CSS屬性錯誤訊息**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 錯誤圖示。 預設為驚歎號。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 錯誤圖示在訊息區域內的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>訊息文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> 訊息內的文字高度。 影響垂直對齊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此訊息支援 `state` 屬性選擇器，其可能值如下： `verifyerror`， `senderror`、和 `sendsuccess`. 屬性選擇器 `verifyerror` 在因內嵌輸入驗證失敗而顯示訊息時設定； `senderror` 設定於後端電子郵件服務回報錯誤時； `sendsuccess` 在成功傳送電子郵件時設定。 如此一來，訊息的樣式可能會因對話方塊狀態而異。

錯誤訊息可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 設定訊息使用十點粗體字型。 而且，它必須有25畫素的行高、20畫素的左邊距、使用驚歎號圖示、紅色文字（如果發生錯誤）、沒有圖示和綠色文字（如果成功）：

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

如果需要垂直捲動，卷軸會呈現在對話方塊右邊緣附近的面板中（由下列CSS類別選取器控制）：

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel
```

**對話方塊捲動面板的CSS屬性**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>捲動面板寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將捲動面板設定為44畫素寬：

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

卷軸區域的外觀是由下列CSS類別選取器所控制：

```
.s7videoviewer .s7emaildialog .s7scrollbar
```

**卷軸的CSS屬性**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 卷軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 垂直卷軸從捲動面板頂端位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直卷軸從捲動面板底部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 水準卷軸從捲動面板的右邊緣位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定寬度為28畫素的卷軸，捲動面板的上、右、下各有8個畫素的邊界：

```
.s7videoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

卷軸軌跡是上下捲動按鈕之間的區域。 元件會自動設定軌跡的位置和高度。 使用下列CSS類別選取器來控制曲目：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**捲動軌跡的CSS屬性**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>磁軌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>軌跡背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定寬度為28畫素且背景為灰色的卷軸軌跡：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

卷軸縮圖在捲動軌跡區域中垂直移動。 其垂直位置完全由元件邏輯控制，但縮圖高度不會隨著內容量而動態變更。 您可以使用以下CSS類別選取器來設定縮圖高度和其他方面：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**卷軸縮圖的CSS屬性**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 磁軌頂端之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定縮圖狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態： `up`， `down`， `over`、和 `disabled`.

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要設定卷軸縮圖，其大小為28 x 45畫素，上下各有10畫素邊界，且每種狀態的圖稿都不同：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上下捲動按鈕的外觀由下列CSS類別選取器控制：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**頂端和底部捲動按鈕的CSS屬性**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>這些按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態： `up`， `down`， `over`、和 `disabled`.

範例 — 若要設定28 x 32畫素的捲動按鈕，且每個狀態的圖稿都不同：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
