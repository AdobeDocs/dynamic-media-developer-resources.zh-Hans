---
title: 連結共用
description: 連結共用工具包含新增至「社交」共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 638ca6c2-375c-4162-b640-68aed6a8a9c6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 2%

---

# 連結共用{#link-share}

連結共用工具包含新增至「社交」共用面板的按鈕，以及工具啟動時顯示的強制回應對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--RICK - Edit to distinguish from previous -->

連結共用按鈕的外觀由下列CSS類別選取器控制：

```css{.line-numbers}
.s7video360viewer .s7linkshare
```

**連結共用工具的CSS屬性**

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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

您可以透過設定從「社交分享」面板移除按鈕 `display:none` CSS屬性的CSS類別。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

範例 — 設定28 x 28畫素的連結共用按鈕，並針對四種不同按鈕狀態分別顯示不同影像：

```css {.line-numbers}
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

使用下列CSS類別選取器控制作用中對話方塊時覆蓋網頁的背景覆蓋：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay
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

**範例**  — 若要將背景覆蓋設為具有70%不透明度的灰色，請執行下列動作：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

依預設，強制回應對話方塊會以案頭系統熒幕的中心顯示，並會使用觸控裝置上的整個網頁區域。 在所有情況下，對話方塊的位置和大小都由元件管理。 此對話方塊由下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialog
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

**範例**  — 若要設定對話方塊以使用整個瀏覽器視窗並在觸控裝置上擁有白色背景：

```css {.line-numbers}
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

對話方塊標頭包含圖示、標題文字和關閉按鈕。 標頭容器由下列CSS類別選擇器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader
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

圖示和標題文字會包裝到使用下列CSS類別選取器控制的額外容器中：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
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

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

標題標題由下列CSS類別選擇器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadertext
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

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7closebutton
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

「關閉」按鈕工具提示和對話方塊標題可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**範例**  — 若要設定含邊框間距的對話方塊標題，請以22 x 12畫素圖示（粗體16點標題）顯示。 最後，還有28 x 28畫素的「關閉」按鈕，此按鈕位於距離對話方塊容器上方的兩個畫素，以及距離右側的兩個畫素：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

對話方塊頁尾包含取消按鈕。 頁尾容器由下列CSS類別選擇器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter
```

**對話方塊頁尾的CSS屬性**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 您可以用來在視覺上分隔頁尾與對話方塊其餘部分的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

頁尾有保留按鈕的內部容器。 它由下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
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

全選按鈕由下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogactionbutton
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

「取消」按鈕由下列CSS類別選擇器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
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

此外，這兩個按鈕共用一個共同的CSS類別，該類別可以包含與其他對話方塊按鈕相同的CSS設定：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
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

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**範例**  — 使用64 x 34取消按鈕設定對話方塊頁尾，每個按鈕狀態的文字顏色和背景顏色不同：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主要對話區域（在頁首和頁尾之間）包含對話內容。 在所有情況下，元件都會管理此區域的寬度，無法在CSS中加以設定。 主要對話方塊區域由下列CSS類別選取器控制：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**對話方塊檢視區域的CSS屬性**

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

**範例**  — 若要將主要對話方塊區域設定為300畫素高度、有10畫素邊界，並使用白色背景：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表單內容（例如標籤和輸入欄位）都位於由以下CSS類別選擇器控制的容器內：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbody
```

**對話方塊主體的CSS屬性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要將表單內容設定為有十個畫素的內距：

```css {.line-numbers}
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

對話方塊表單中的所有靜態標籤都由控制

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

此類別不適合控制標籤大小或位置，因為您可以將其套用至表單使用者介面不同位置的文字。

**對話方塊標籤的CSS屬性**

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

對話方塊標籤可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**範例**  — 若要將所有標籤設定為灰色、粗體加九畫素字型：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

顯示在連結頂端的文字復本大小由下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**對話方塊輸入範圍欄位的CSS屬性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>文字寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要將文字複製設定為430畫素寬，並在底部有10畫素邊框間距：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共用連結會包裝在容器中，並使用下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**對話方塊輸入容器的CSS屬性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>共用連結容器周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要在內嵌程式碼文字周圍設定一畫素灰色邊框，且邊框間距為9畫素：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共用連結本身由下列CSS類別選取器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink
```

**對話方塊共用連結的CSS屬性**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>共用連結寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 將共用連結設定為450畫素寬：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
