---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>資訊伺服器URL範本是用來擷取資訊面板內容範本中變數替代的索引鍵/值組。 指定的範本通常包含巨集預留位置，這些預留位置會在請求傳送至伺服器之前被實際資料取代。 </p> <p><span class="codeph"> $1$</span> 會取代為觸發下列專案的滑鼠指向效果值： <span class="codeph"> InfoPanelPopup</span> 啟用。 </p> <p><span class="codeph"> $2$</span> 會取代為影像集中目前影格的序號。 </p> <p><span class="codeph"> $3$</span> 會取代為目前專案的父項集名稱中指定的第一個路徑元素。 通常會對應至目錄ID。 </p> <p><span class="codeph"> $4$</span> 會以路徑中的下列元素取代，且會對應至資產id。 實際的資訊伺服器要求語法取決於資訊伺服器，而且伺服器之間有所不同。 例如，以下是典型的Dynamic Media資訊伺服器請求範本： </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定資訊面板快顯視窗時，傳遞至資訊面板的HTML代碼和JavaScript代碼會在使用者端電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-71356e3c13244e62b0582980d9d05328}

可选.

## 默认 {#section-22e9af803f724434807d34e200eb7518}

无。

## 示例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
