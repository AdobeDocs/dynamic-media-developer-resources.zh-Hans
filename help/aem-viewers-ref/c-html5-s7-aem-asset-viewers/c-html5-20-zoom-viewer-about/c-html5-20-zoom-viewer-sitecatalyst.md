---
title: 支持Adobe Analytics跟踪
description: 支持Adobe Analytics跟踪
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
TQID: 'https://experienceleague.adobe.com/4XIzFFsX43NZBy4uB5WRZeIs92EWpbT8U2BsnTsmlDU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

## 开箱即用跟踪 {#section-ba994f079d0343c8ae48adffaa3195a3}

视频查看器支持[!DNL Adobe Analytics]开箱即用跟踪。 要启用跟踪，请将适当的公司预设名称作为`config2`参数传递。

查看器还会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调，并根据需要处理回调函数的`eventInfo`参数。 以下代码是此类处理程序函数的示例：

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

查看器跟踪以下SDK用户事件：

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK用户事件 </p> </th> 
   <th colname="col2" class="entry"> <p>发送时间…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">加载</span> </p> </td> 
   <td colname="col2"> <p>首先加载查看器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">交换</span> </p> </td> 
   <td colname="col2"> <p>在查看器中使用<span class="codeph"> setAsset() </span> API交换资源。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">缩放</span> </p> </td> 
   <td colname="col2"> <p> 缩放图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">平移</span> </p> </td> 
   <td colname="col2"> <p>图像被平移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">样本</span> </p> </td> 
   <td colname="col2"> <p> 通过单击或点按色板可更改图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

