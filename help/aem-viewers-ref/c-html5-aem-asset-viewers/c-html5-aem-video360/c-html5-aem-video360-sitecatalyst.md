---
title: 支持Adobe Analytics跟踪
description: 支持Adobe Analytics跟踪
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

默认情况下，查看器会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调，并根据需要处理回调函数的`eventInfo`参数。 以下代码是此类处理程序函数的示例：

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
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
   <th colname="col2" class="entry"> <p>已发送…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">加载</span> </p> </td> 
   <td colname="col2"> <p>首次加载查看器时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">交换</span> </p> </td> 
   <td colname="col2"> <p>在使用<span class="codeph"> setAsset() </span> API在查看器中交换资产时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">播放</span> </p> </td> 
   <td colname="col2"> <p>播放开始时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">暂停</span> </p> </td> 
   <td colname="col2"> <p>暂停播放时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">停止</span> </p> </td> 
   <td colname="col2"> <p>停止播放时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">里程碑</span> </p> </td> 
   <td colname="col2"> <p>当播放达到以下里程碑之一时：0%、25%、50%、75%或100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH </span> </p> </td> 
   <td colname="col2"> <p>用户每次单击交互式样本时。 </p> </td> 
  </tr> 
 </tbody> 
</table>
