---
description: 支持Adobe Analytics跟踪
solution: Experience Manager
title: 支持Adobe Analytics跟踪
uuid: a7de5549-2a9d-4153-be5e-72705ced85ac
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，业务从业者，数据工程师，数据架构师
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

## 自定义跟踪{#section-cda48fc9730142d0bb3326bac7df3271}

默认情况下，查看器会向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调并根据需要处理回调函数的`eventInfo`参数。 下面的代码就是此类处理函数的一个示例：

```
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

查看器跟踪以下SDK用户事件:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK用户事件 </p> </th> 
   <th colname="col2" class="entry"> <p>在…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>首先加载查看器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 横幅  </span> </p> </td> 
   <td colname="col2"> <p>轮盘横幅图像已更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>用户激活热点。 </p> </td> 
  </tr> 
 </tbody> 
</table>

