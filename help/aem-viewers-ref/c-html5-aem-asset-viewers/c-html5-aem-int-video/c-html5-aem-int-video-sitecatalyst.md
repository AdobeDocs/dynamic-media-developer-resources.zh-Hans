---
title: 支援Adobe Analytics追蹤
description: HTML5 Video360檢視器支援Adobe Analytics立即可用的追蹤功能。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

HTML5 Video360檢視器支援Adobe Analytics立即可用的追蹤功能。

若要啟用追蹤，請將適當的公司預設集名稱傳遞為 `config2` 引數。

依預設，檢視器會傳送單一追蹤HTTP要求至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，請務必監聽 `trackEvent` 檢視器回呼並處理 `eventInfo` 必要時，回呼函式的引數。 下列程式碼是此類處理常式函式的範例：

```javascript {.line-numbers}
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
   <th colname="col2" class="entry"> <p>已发送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>先載入檢視器時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>當在檢視器中使用交換資產時 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放開始時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>暫停播放時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>播放停止時。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>當播放達到以下里程碑之一時：0%、25%、50%、75%或100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>
