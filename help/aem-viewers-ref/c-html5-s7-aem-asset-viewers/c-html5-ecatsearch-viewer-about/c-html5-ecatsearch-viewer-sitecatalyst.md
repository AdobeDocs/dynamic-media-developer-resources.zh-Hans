---
description: eCatalog Search Viewer支持Adobe Analytics的即装即用跟踪。
seo-description: eCatalog Search Viewer支持Adobe Analytics的即装即用跟踪。
seo-title: 支持Adobe Analytics跟踪
solution: Experience Manager
title: 支持Adobe Analytics跟踪
topic: Dynamic media
uuid: 2e1e2bc6-5372-4ba2-b6d7-8b760b1b0a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

eCatalog Search Viewer支持Adobe Analytics的即装即用跟踪。

## 现成跟踪 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog Search Viewer支 [!DNL Adobe Analytics] 持现成跟踪。 要启用跟踪，请将正确的公司预设名称作为参 `config2` 数传递。

查看器还向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听查看器回调，并 `trackEvent` 根据需要处 `eventInfo` 理回调函数的参数。 以下代码就是此类处理函数的示例：

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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

查看器跟踪以下SDK用户事件:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK用户事件 </p> </th> 
   <th colname="col2" class="entry"> <p>发送时间…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>查看器先加载。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>在查看器中，会使用 <span class="codeph"> setAsset() </span> API交换资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 缩放 </span> </p> </td> 
   <td colname="col2"> <p> 图像被缩放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 平移 </span> </p> </td> 
   <td colname="col2"> <p>图像被平移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 样本 </span> </p> </td> 
   <td colname="col2"> <p> 通过单击或点按色板来更改图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAGE </span> </p> </td> 
   <td colname="col2"> <p> 当前帧在主视图中发生更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM </span> </p> </td> 
   <td colname="col2"> <p>信息面板弹出窗口被激活。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>用户因单击图像映射而导航到其他页面。 </p> </td> 
  </tr> 
 </tbody> 
</table>

