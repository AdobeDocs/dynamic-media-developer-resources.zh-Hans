---
title: 支援Adobe Analytics追蹤
description: 彈出式檢視器支援立即可用的Adobe Analytics追蹤。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User,Data Engineer,Data Architect
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---

# 支援Adobe Analytics追蹤{#support-for-adobe-analytics-tracking}

彈出式檢視器支援立即可用的Adobe Analytics追蹤。

## 現成可用的追蹤 {#section-ba994f079d0343c8ae48adffaa3195a3}

彈出式檢視器支援 [!DNL Adobe Analytics] 追蹤現成可用的專案。 若要啟用追蹤，請將適當的公司預設集名稱傳遞為 `config2` 引數。

檢視器也會傳送單一追蹤HTTP要求至已設定的影像伺服器，並提供檢視器型別和版本資訊。

## 自訂追蹤 {#section-cda48fc9730142d0bb3326bac7df3271}

若要與協力廠商分析系統整合，請務必監聽 `trackEvent` 檢視器回呼並處理 `eventInfo` 必要時，回呼函式的引數。 下列程式碼是此類處理常式函式的範例：

```javascript {.line-numbers}
var flyoutViewer = new s7viewers.FlyoutViewer({ 
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
   <td colname="col2"> <p>在檢視器中交換資產時，使用 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 缩放 </span> </p> </td> 
   <td colname="col2"> <p>彈出專案已啟動或縮放等級已變更。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 平移 </span> </p> </td> 
   <td colname="col2"> <p> 已平移影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 样本 </span> </p> </td> 
   <td colname="col2"> <p> 按一下或點選色票即可變更影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>
