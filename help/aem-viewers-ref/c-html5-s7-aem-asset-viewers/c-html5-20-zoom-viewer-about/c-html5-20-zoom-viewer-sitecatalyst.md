---
title: 支援Adobe Analytics追蹤
description: 支援Adobe Analytics追蹤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

## 現成可用的追蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

Video Viewer支援 [!DNL Adobe Analytics] 追蹤現成可用的專案。 若要啟用追蹤，請將適當的公司預設集名稱傳遞為 `config2` 引數。

檢視器也會傳送單一追蹤HTTP要求至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，請務必監聽 `trackEvent` 檢視器回呼並處理 `eventInfo` 必要時，回呼函式的引數。 下列程式碼是此類處理常式函式的範例：

```javascript {.line-numbers}
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>在檢視器中使用交換資產 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 缩放 </span> </p> </td> 
   <td colname="col2"> <p> 影像會縮放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 平移 </span> </p> </td> 
   <td colname="col2"> <p>已平移影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 样本 </span> </p> </td> 
   <td colname="col2"> <p> 按一下或點選色票即可變更影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>
