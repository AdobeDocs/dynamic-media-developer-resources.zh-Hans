---
title: 視訊筆畫壓感
description: 視訊筆畫壓感是水準滑桿控制項，可讓使用者動態搜尋目前播放視訊內的任何時間位置
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 2%

---

# 視訊筆畫壓感{#video-scrubber}

視訊筆畫壓感是水準滑桿控制項，可讓使用者動態搜尋目前播放視訊內的任何時間位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

清除器「旋鈕」也會隨著視訊播放而移動，以指出視訊在播放期間的目前時間位置。 視訊筆畫壓感一律採用控制列的整個寬度。 您可以透過CSS建立視訊筆畫壓感的外觀，並變更其高度和垂直位置。

視訊筆畫壓感的一般外觀是由下列CSS類別選取器所控制：

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**視訊筆畫壓感的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>視訊清除程式的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>視訊筆畫壓感色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選取器會追蹤背景、播放和載入指標：

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**曲目的CSS屬性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>對應軌道的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>對應曲目的色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器會控制旋鈕：

```
.s7videoviewer .s7videoscrubber .s7knob
```

**旋鈕的CSS屬性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>垂直旋鈕位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>旋鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>旋鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>旋鈕圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器可控制播放時間泡泡：

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**時間播放泡泡的CSS屬性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>泡泡圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>文字與泡泡區域的對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

視訊筆畫壓感工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

**範例**  — 使用自訂軌跡顏色的視訊筆畫壓感來設定視訊檢視器。 筆畫壓感必須有10個畫素高，並且位於距離控制列頂端和左側邊緣10個畫素和35個畫素的位置。

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

使用啟用視訊章節時 `navigation` 引數，章節位置會在視訊筆畫壓感軌跡上方顯示為標籤。

視訊章節標籤是由下列CSS類別選擇器所控制：

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**視訊章節標籤的CSS屬性**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標籤寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標籤高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>影片章節標籤圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援 `state` 屬性選取器，可用來將不同的外觀元素套用至不同的按鈕狀態。 尤其是， `selected='default'` 對應至預設的視訊章節標籤狀態和 `selected='over'` 當滑鼠懸停或觸控手勢啟動視訊章節標籤時使用。

**範例**  — 設定5 x 8畫素的視訊章節標籤，並在「預設」和「超過」狀態使用不同的圖片。

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

影片章節泡泡位於影片章節標籤上方，並顯示指定章節的標題、開始時間和說明。 您可以控制相對於視訊筆畫壓感軌跡的最大泡泡寬度和垂直位移。 其餘由元件自動計算。

視訊章節泡泡由下列CSS類別選擇器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**視訊章節泡泡的CSS屬性**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>視訊章節泡泡的最大寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從視訊筆畫壓感軌跡的垂直位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定寬235畫素、且從視訊筆畫壓感軌跡底部往上八畫素的視訊章節泡泡。

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

影片章節泡泡圖包含選用的標題和內容。 標題具有可選的章節開始時間和章節標題。

標頭由以下CSS類別選擇器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**視訊章節泡泡標題的CSS屬性**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>影片章節泡泡標題高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>視訊章節泡泡標題文字的內部邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>影片章節泡泡標題背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>視訊章節泡泡圖示頭文字行高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定高22畫素、行高22畫素、水準邊界12畫素和灰色背景的視訊章節泡泡標題。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

視訊章節的開始時間由下列CSS類別選取器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**視訊章節開始時間的CSS屬性**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文字色彩。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 右內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 開始時間和章節標題之間的內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定章節開始時間，請使用灰色10畫素Verdana字型，並在右側有10畫素邊框間距。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

視訊章節標題由下列CSS類別選擇器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**視訊章節標題的CSS屬性**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標題文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標題字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>視訊章節標題字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>影片章節標題字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 設定使用白色、粗體、10畫素Verdana字型的視訊章節標題。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

視訊章節說明由下列CSS類別選擇器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**視訊章節說明的CSS屬性**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>影片章節說明文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>影片章節說明背景色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>影片章節說明字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>視訊章節說明字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>影片章節說明行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>影片章節說明內邊距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 使用深灰色11畫素Verdana字型搭配淺灰色背景來設定視訊章節說明。 最後，使用5個畫素的行高、12個畫素的水準邊框間距、12個畫素的上邊框間距和9個畫素的下邊框間距。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

章節泡泡底部的楔形聯結器由以下CSS類別選取器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**楔形聯結器的CSS屬性**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>楔形聯結器顏色。 </p> <p>定義為 <span class="codeph"> &lt;color&gt; 透明 </span> 因此只定義上邊框顏色，其餘邊框則保持透明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> 楔形聯結器寬度。 </p> <p>定義為 <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> 因此只為頂端和水準框線定義相同的寬度，而底端框線寬度為 <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 僅定義負下邊界。 其值應與 <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 若要設定灰色、6畫素楔形聯結器：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
