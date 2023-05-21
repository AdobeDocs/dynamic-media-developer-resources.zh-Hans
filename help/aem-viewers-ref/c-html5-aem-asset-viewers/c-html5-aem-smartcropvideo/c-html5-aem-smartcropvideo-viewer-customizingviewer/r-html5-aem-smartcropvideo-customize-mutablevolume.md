---
title: 可變音量
description: 可靜音的音量控制最初會顯示為一個按鈕，讓使用者將智慧型裁切視訊播放器聲音設為靜音或取消靜音。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e0a3e849-842b-4137-acc2-34301e89518f
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 2%

---

# 可變音量{#mutable-volume}

可靜音的音量控制最初會顯示為一個按鈕，讓使用者將智慧型裁切視訊播放器聲音設為靜音或取消靜音。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

當使用者將滑鼠移到按鈕上時，會出現一個滑桿，讓使用者可以設定音量。 可變音量控制項可以相對於包含它的控制列，由CSS來調整大小、外觀和定位。

可變體積塊區域的外觀由下列CSS類別選取器控制：

```
.s7smartcropvideoviewer .s7mutablevolume
```

**可變磁碟區的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 從右邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 可變音量控制的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>可變音量控制項的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 可變音量控制的色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

靜音/取消靜音按鈕外觀由以下CSS類別選擇器控制：

```
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton
```

您可以控制每個按鈕狀態的背景影像。 按鈕的大小繼承自磁碟區控制項的大小。

**按鈕影像的CSS屬性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕同時支援 `state` 和 `selected` 屬性選取器，可將不同的外觀元素套用至不同的按鈕狀態。 尤其是， `selected='true'` 對應至「靜音」狀態和 `selected='false'` 對應至「未靜音」狀態。

垂直音量列區域由下列CSS類別選取器控制：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume
```

**垂直體積塊列區域的CSS屬性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積塊的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積塊的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 垂直體積塊的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直音量控制內的音軌由下列CSS類別選取器控制：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**垂直音量控制項的CSS屬性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控制的背景色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直音量旋鈕由下列CSS類別選取器控制：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**垂直音量控制旋鈕的CSS屬性**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控制旋鈕圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋鈕的水平位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定靜音按鈕，其位置為32 x 32畫素，從上到下為6畫素，從控制列的右邊緣為38畫素。 選取或未選取時，針對四種不同按鈕狀態分別顯示不同的影像。

```
.s7smartcropvideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

以下是如何在可變音量控制項中設定音量滑桿樣式的範例。

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

以下是如何自訂視訊播放器的範例，以便在播放期間停用音效。 將下列程式碼新增至檢視器的內嵌程式碼：

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

在上面的程式碼範例中，音量等級設定為 `0` 於 `mutableVolume` 元件。 然後，相同的元件會停用，因此一般使用者無法使用該元件。
