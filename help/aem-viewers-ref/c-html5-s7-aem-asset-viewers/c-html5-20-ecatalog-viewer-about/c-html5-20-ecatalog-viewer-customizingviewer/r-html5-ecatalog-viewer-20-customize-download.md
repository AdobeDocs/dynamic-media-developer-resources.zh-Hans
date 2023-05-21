---
title: 下载
description: 下载
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fb01371b-0aa6-4591-8523-120c217cf45d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 下载{#download}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「下載」按鈕的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7download
```

**下載按鈕的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂端邊界 </span> </p> </td> 
   <td colname="col2"> <p> 從控制列頂端的位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊界 </span> </p> </td> 
   <td colname="col2"> <p> 與左側或控制列左側的下一個按鈕（如果它是列中的第一個按鈕）的距離。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

範例 — 設定28 x 28畫素的「下載」按鈕，並針對四種不同按鈕狀態分別顯示不同影像：

```
.s7ecatalogviewer .s7download { 
 margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7download[state='up'] { 
background-image:url(images/v2/Dowmload_dark_up.png); 
} 
.s7ecatalogviewer .s7download[state='over'] { 
background-image:url(images/v2/Dowmload_dark_over.png); 
} 
.s7ecatalogviewer .s7download[state='down'] { 
background-image:url(images/v2/Dowmload_dark_down.png); 
} 
.s7ecatalogviewer .s7download[state='disabled'] { 
background-image:url(images/v2/Dowmload_dark_disabled.png); 
}
```
