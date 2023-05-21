---
title: Video360播放器
description: 視訊播放器是檢視器中顯示視訊內容的矩形區域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# Video360播放器{#video-player}

視訊播放器是檢視器中顯示視訊內容的矩形區域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的視訊尺寸不符合視訊播放器的尺寸，則視訊內容會置中於視訊播放器的矩形顯示區域中。

下列CSS類別選擇器可控制視訊播放器的外觀：

```
.s7video360viewer .s7video360player
```

**視訊播放器的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>主檢視的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以將系統無法播放視訊時所顯示的錯誤訊息當地語系化。

另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

範例 — 若要設定視訊檢視器，且視訊播放器大小設定為512 x 288畫素。

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

緩衝動畫的外觀由下列CSS類別選取器控制：

```
.s7video360viewer .s7video360player .s7waiticon
```

**等待圖示的CSS屬性**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊界 </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示左側邊界，通常減去圖示寬度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂端邊界 </span> </p> </td> 
   <td colname="col2"> <p> 動畫圖示上方邊界，通常減去圖示高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 旋鈕圖稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將緩衝動畫設定為寬101畫素、高29畫素：

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
