---
title: 事件回呼
description: 事件回呼
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e87b2a84-735c-4412-a4dd-97b18474a1d2
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行階段行為的JavaScript事件回呼。

回呼處理常式是透過傳遞事件名稱和對應的處理常式函式來指派 `handlers` 屬性至 `config` 檢視器建構函式中的JSON物件。 或者，也可以使用 `setHandlers()` api方法。

支援的檢視器事件包括：

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>查看器事件 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>當檢視器初始化完成並建立所有內部元件時觸發，以便使用 <span class="codeph"> getComponent() </span> API。 回呼處理常式不接受任何引數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> 事件追蹤系統(例如Adobe Analytics)可處理檢視器內每次發生事件時都會觸發。 回呼處理常式接受下列引數： </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> 物件ID {String} </span>  — 目前未使用。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span>  — 目前未使用。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span>  — 觸發事件之Viewer SDK元件的執行個體名稱。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> 時間戳記{Number} </span>  — 事件時間戳記。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span>  — 事件裝載。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> 當使用者啟動連結區且連結快速檢視資料時觸發。 回呼處理常式會採用下列引數： </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> 資料{Object} </span>  — 包含熱點定義之資料的JSON物件。 欄位 <span class="codeph"> sku </span> 是必填欄位，其他欄位則是選用欄位，且取決於來源熱點定義。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參閱 [Carouselviewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) 和 [setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
