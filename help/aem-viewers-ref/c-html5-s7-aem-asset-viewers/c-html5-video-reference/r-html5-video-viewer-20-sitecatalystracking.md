---
description: 视频查看器支持Adobe Analytics开箱即用跟踪。
seo-description: 视频查看器支持Adobe Analytics开箱即用跟踪。
seo-title: 支持Adobe Analytics跟踪
solution: Experience Manager
title: 支持Adobe Analytics跟踪
topic: Dynamic Media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

视频查看器支持Adobe Analytics开箱即用跟踪。

## 现成跟踪{#section-3b101fe30be943c1b679fd5c273569ca}

视频查看器支持Adobe Analytics开箱即用跟踪。

要启用跟踪，请将正确的公司预设名称传递为`config2`参数。

查看器还向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪{#section-ab10bd7caf184721a366cf3953071934}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调并根据需要处理回调函数的`eventInfo`参数。 下面的代码就是此类处理函数的一个示例：

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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
   <td colname="col2"> <p>使用<span class="codeph"> setAsset()</span> API在查看器中交换资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>开始播放。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放已暂停。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>播放停止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>播放达到以下重点之一：0%、25%、50%、75%和100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

