---
title: 內嵌共用
description: 內嵌共用工具包含新增至Social共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e29a81b8-67f3-4367-b21c-d5902420bc85
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '2585'
ht-degree: 2%

---

# 內嵌共用{#embed-share}

內嵌共用工具包含新增至Social共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

內嵌共用按鈕的外觀由以下CSS類別選取器控制：

```
.s7videoviewer .s7embedshare
```

**內嵌共用工具的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
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

您可以透過設定從「社交分享」面板移除按鈕 `display:none` CSS屬性的CSS類別。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要設定內嵌共用按鈕（28 x 28畫素），並針對四種不同按鈕狀態分別顯示不同影像：

```
.s7videoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7videoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7videoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7videoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

使用下列CSS類別選取器可控制對話方塊啟動時覆蓋網頁的背景覆蓋：

```
.s7videoviewer .s7embeddialog .s7backoverlay
```

**背景覆蓋的CSS屬性**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>背景覆蓋顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將背景覆蓋設定為具有70%不透明度的灰色：

```
.s7videoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

依預設，強制回應對話方塊會以案頭系統熒幕的中心顯示，並會使用觸控裝置上的整個網頁區域。 在所有情況下，對話方塊的位置和大小都由元件管理。 此對話方塊由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialog
```

**對話方塊的CSS屬性**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 對話方塊邊框半徑（如果對話方塊未取用整個瀏覽器）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>對話方塊背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>應取消設定或設為100%，此時對話方塊會取用整個瀏覽器視窗（觸控裝置偏好此模式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>應取消設定或設為100%，此時對話方塊會取用整個瀏覽器視窗（觸控裝置偏好此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定對話方塊以使用整個瀏覽器視窗並在觸控裝置上擁有白色背景：

```
.s7videoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

對話方塊標頭包含圖示、標題文字和關閉按鈕。 標題容器的控制方式

```
.s7videoviewer .s7embeddialog .s7dialogheader
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
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline
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
.s7videoviewer .s7embeddialog .s7dialogheadericon
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
.s7videoviewer .s7embeddialog .s7dialogheadertext
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
.s7videoviewer .s7embeddialog .s7closebutton
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

範例 — 若要設定含邊框間距的對話方塊標題，請以24 x 14畫素圖示、粗體16點標題顯示。 最後，還有28 x 28畫素的關閉按鈕，從上方放置兩個畫素，從對話方塊容器的右側放置兩個畫素：

```
.s7videoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話方塊頁尾包含「取消」按鈕。 頁尾容器由下列CSS類別選擇器控制：

```
.s7videoviewer .s7embeddialog .s7dialogfooter
```

**對話方塊頁尾**的CSS屬性

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 您可以用來在視覺上分隔頁尾與對話方塊其餘部分的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

頁尾有保留按鈕的內部容器。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**對話方塊按鈕容器的CSS屬性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 頁尾與按鈕之間的內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「選取全部」按鈕由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialogactionbutton
```

此按鈕僅在桌上型電腦系統上可用。

**全選按鈕的CSS屬性**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>全選按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

取消按鈕由下列CSS類別選擇器控制：

```
.s7videoviewer .s7embeddialog .s7dialogcancelbutton
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
>取消按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

此外，這兩個按鈕共用共用的CSS類別可以包含與其他對話方塊按鈕相同的CSS設定：

```
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button
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

範例 — 若要設定具有64 x 34 Cancel按鈕的對話方塊頁尾，讓每個按鈕狀態的文字顏色和背景顏色不同：

```
.s7videoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主要對話方塊區域（在頁首和頁尾之間）右側包含可捲動對話方塊內容和捲動面板。 在任何情況下，元件都會管理此區域的寬度，無法在CSS中加以設定。 主要對話方塊區域由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialogviewarea
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

範例 — 若要將主要對話方塊區域設定為300畫素高度、有10畫素邊界，並使用白色背景：

```
.s7videoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表單內容（例如標籤和輸入欄位）都位在容器內，由控制

```
.s7videoviewer .s7embeddialog .s7dialogbody
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
.s7videoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

對話方塊表單中的所有靜態標籤都由控制

```
.s7videoviewer .s7embeddialog .s7dialoglabel
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

對話方塊標籤工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 將所有標籤設定為灰色、粗體加九畫素字型：

```
.s7videoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

顯示在內嵌程式碼頂端的文字復本大小，由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialoginputwide
```

**對話方塊輸入範圍欄位的CSS屬性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將文字副本設定為430畫素寬，並在底部有十個畫素的邊框間距：

```
.s7videoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

內嵌程式碼會包裝在容器中，並使用下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**對話方塊輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>內嵌程式碼容器的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>內嵌程式碼容器周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要在內嵌程式碼文字周圍設定一個畫素的灰色邊框，請使其寬度430畫素，並加上十畫素邊框間距：

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

實際的內嵌程式碼文字由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**對話方塊輸入容器的CSS屬性**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動換行 </span> </p> </td> 
   <td colname="col2"> <p>文字環繞樣式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定內嵌程式碼，以便使用 `break-word` 自動換行：

```
.s7videoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

內嵌大小標籤和下拉式清單位於對話方塊底部，並放入由以下CSS類別選取器控制的容器中：

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**對話方塊內嵌大小面板的CSS屬性**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定內嵌大小面板，使其有10個畫素的內距：

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

內嵌大小標籤的大小和對齊方式由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**對話方塊內嵌大小面板的CSS屬性**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>垂直標籤對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>標籤寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將內嵌大小標籤設定為靠上對齊和80畫素寬：

```
.s7videoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

內嵌大小下拉式方塊的寬度由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7combobox
```

**下拉式方塊的CSS屬性**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>下拉式方塊寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>下拉式方塊支援 `expanded` 屬性選擇器，可能的值為 `true` 和 `false`. 此 `true` 當下拉式方塊顯示預先定義的內嵌大小之一時使用value，因此應採用所有可用寬度。 此 `false` 當在下拉式方塊中選取自訂大小選項時會使用值，因此應將其縮小以允許為自訂寬度和高度輸入欄位使用空間。

範例 — 若要將內嵌大小下拉式方塊設定為在顯示預先定義的專案時為300畫素寬，而在顯示自訂大小時為110畫素寬：

```
.s7videoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7videoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

下拉式方塊文字的高度是由特殊內部元素定義，並且由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**下拉式方塊文字的CSS屬性**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>下拉式方塊文字高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將內嵌大小下拉式方塊文字高度設定為40畫素：

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

下拉式方塊右側有一個「下拉」按鈕，它由以下CSS類別選擇器控制：

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**下拉式方塊按鈕的CSS屬性**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>下拉式方塊內的垂直按鈕位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>組合方塊內的水準按鈕位置。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>每個狀態的按鈕影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

範例 — 若要將「下拉」按鈕設為28 x 28畫素，並為每個狀態設定個別影像：

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

在開啟下拉式方塊時會顯示內嵌大小清單的面板，由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown
```

面板的大小和位置由元件控制。 無法透過CSS變更它。

**下拉式方塊的CSS屬性**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>面板邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將下拉式方塊面板設定為一個畫素灰色邊框：

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

下拉式面板中的單一專案，由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor
```

**下拉式專案錨點的CSS屬性**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>專案背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將下拉式方塊面板專案設定為白色背景：

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

在下拉式方塊面板內所選專案左側顯示的核取標籤，由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7checkmark
```

**核取方塊的CSS屬性**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>專案影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將勾號圖示設定為25 x 25畫素：

```
.s7videoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

在內嵌大小下拉式方塊中選取「自訂大小」選項時，對話方塊右側會顯示兩個額外的輸入欄位，以讓使用者輸入自訂內嵌大小。 這些欄位會包裝在容器中，而容器是由下列CSS類別選取器所控制：

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**對話方塊自訂大小面板的CSS屬性**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p> 與內嵌大小下拉式方塊的距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將自訂大小輸入欄位面板設定為下拉式方塊右側的20畫素：

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

每個自訂大小輸入欄位都會包裝在容器中，以呈現框線並設定欄位之間的邊界。 它由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize
```

**對話方塊自訂大小的CSS屬性**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>輸入欄位周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 輸入欄位寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 輸入欄位邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 輸入欄位內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定自訂大小輸入欄位，使其有一個畫素灰色邊框、邊界、邊框間距，以及寬度為70畫素：

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

如果需要垂直捲動，卷軸會呈現在對話方塊右邊緣附近的面板中（使用下列CSS類別選取器控制）：

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel
```

**對話方塊捲動面板的CSS屬性**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>捲動面板寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將捲動面板設定為44畫素寬

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

卷軸區域的外觀是由下列CSS類別選取器所控制：

```
.s7videoviewer .s7embeddialog .s7scrollbar
```

**卷軸的CSS屬性**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>卷軸寬度。 </p> </td> 
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

範例 — 若要設定寬度為28畫素的卷軸，且卷軸面板的上下左右各有8個畫素的邊界：

```
.s7videoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

卷軸軌跡是上下捲動按鈕之間的區域。 元件會自動設定軌跡的位置和高度。 使用下列CSS類別選取器來控制曲目

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**卷軸軌跡的CSS屬性**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>磁軌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 追蹤背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定寬度為28畫素且背景為灰色的卷軸軌跡：

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

卷軸縮圖在捲動軌跡區域中垂直移動。 其垂直位置完全由元件邏輯控制。 不過，縮圖高度不會隨著內容量而動態變更。 您可以使用以下CSS類別選取器來設定縮圖高度和其他方面：

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**卷軸縮圖的CSS屬性**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
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
   <td colname="col2"> <p>磁軌頂端之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定縮圖狀態顯示的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態： `up`， `down`， `over`、和 `disabled`.

範例 — 若要設定卷軸縮圖，其大小為28 x 45畫素，上下各有10畫素邊界，且每種狀態的圖稿都不同：

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上下捲動按鈕的外觀由下列CSS類別選取器控制：

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

無法使用CSS top、left、bottom和right屬性來定位捲動按鈕。 相反地，檢視器邏輯會自動定位它們。

**頂端和底部捲動按鈕的CSS屬性**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
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

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

範例 — 若要設定28 x 32畫素的捲動按鈕，且每個狀態的圖稿都不同：

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
