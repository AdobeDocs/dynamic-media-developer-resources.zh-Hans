---
description: HTML5 Video360查看器支持Adobe Analytics现成跟踪。
solution: Experience Manager
title: 支持Adobe Analytics跟踪
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，业务从业者，数据工程师，数据架构师
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

HTML5 Video360查看器支持Adobe Analytics现成跟踪。

要启用跟踪，请将正确的公司预设名称作为`config2`参数进行传递。

默认情况下，查看器向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪{#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调并根据需要处理回调函数的`eventInfo`参数。 下面的代码就是此类处理函数的一个示例：

```
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

查看器跟踪以下SDK用户事件:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK用户事件 </p> </th> 
   <th colname="col2" class="entry"> <p>已发送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>查看器时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>使用<span class="codeph"> setAsset()</span> API在查看器中交换资产时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>播放开始。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>播放暂停时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>停止播放时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>当播放达到以下里程碑之一时：0%、25%、50%、75%或100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

