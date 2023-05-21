---
title: twitter共用
description: twitter共用工具包含新增至「社交共用」面板的按鈕。 選取按鈕後，使用者會重新導向至社交服務提供的「共用」對話方塊。 按鈕的位置可完全由社交分享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a90a4c82-b51a-4fb0-9196-44ae4ba8e0cd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# twitter共用{#twitter-share}

twitter共用工具包含新增至「社交共用」面板的按鈕。 選取按鈕後，使用者會重新導向至社交服務提供的「共用」對話方塊。 按鈕的位置可完全由社交分享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

twitter共用按鈕的外觀由下列CSS類別選擇器控制：

```
.s7video360viewer .s7twittershare
```

**twitter共用工具的CSS屬性**

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

**範例**  — 若要設定28 x 28畫素的Twitter共用按鈕，並針對四種不同按鈕狀態分別顯示不同影像：

```
.s7video360viewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7video360viewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7video360viewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7video360viewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
