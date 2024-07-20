---
title: 支持Adobe Analytics跟踪
description: 混合媒体查看器支持开箱即用的Adobe Analytics跟踪。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 3b28c853-3747-4805-a141-3cce1398d783
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

混合媒体查看器支持开箱即用的Adobe Analytics跟踪。

## 开箱即用跟踪 {#section-ba994f079d0343c8ae48adffaa3195a3}

混合媒体查看器支持[!DNL Adobe Analytics]开箱即用跟踪。 要启用跟踪，请将适当的公司预设名称作为`config2`参数传递。

查看器还会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调，并根据需要处理回调函数的`eventInfo`参数。 以下代码是此类处理程序函数的示例：

```javascript {.line-numbers}
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col2"> <p>缩放图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">平移</span> </p> </td> 
   <td colname="col2"> <p>图像被平移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">样本</span> </p> </td> 
   <td colname="col2"> <p> 通过单击或点按色板可更改图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">播放</span> </p> </td> 
   <td colname="col2"> <p>开始播放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">暂停</span> </p> </td> 
   <td colname="col2"> <p>播放已暂停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">停止</span> </p> </td> 
   <td colname="col2"> <p>播放已停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">里程碑</span> </p> </td> 
   <td colname="col2"> <p>播放达到以下毫石之一：0%、25%、50%、75%和100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">旋转</span> </p> </td> 
   <td colname="col2"> <p>执行旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>
