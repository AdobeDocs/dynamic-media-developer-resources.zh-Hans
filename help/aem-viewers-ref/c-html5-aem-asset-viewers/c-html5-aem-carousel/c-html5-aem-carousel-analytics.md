---
title: 支援Adobe Analytics追蹤
description: 支援Adobe Analytics追蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User,Data Engineer,Data Architect
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 1%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

依預設，檢視器會傳送單一追蹤HTTP請求給已設定的影像伺服器，其中包含檢視器型別和版本資訊。

若要與協力廠商分析系統整合，請務必監聽 `trackEvent` 檢視器回呼並處理 `eventInfo` 必要時，回呼函式的引數。 下列程式碼是此類處理常式函式的範例：

```java {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

檢視器會追蹤下列SDK使用者事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK使用者事件 </p> </th> 
   <th colname="col2" class="entry"> <p>傳送時間…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>檢視器會先載入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 橫幅 </span> </p> </td> 
   <td colname="col2"> <p>輪播橫幅影像已變更。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>使用者會啟動熱點。 </p> </td> 
  </tr> 
 </tbody> 
</table>
