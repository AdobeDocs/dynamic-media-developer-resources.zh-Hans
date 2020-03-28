---
description: 旋转查看器支持Adobe Analytics开箱即用跟踪。
seo-description: 旋转查看器支持Adobe Analytics开箱即用跟踪。
seo-title: 支持Adobe Analytics跟踪
solution: Experience Manager
title: 支持Adobe Analytics跟踪
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

旋转查看器支持Adobe Analytics开箱即用跟踪。

## 现成跟踪 {#section-d06145cfa2b9491bb485b599368d466e}

旋转查看器支持Adobe Analytics现成跟踪。

要启用跟踪，请将正确的公司预设名称作为参 `config2` 数传递。

查看器还向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-47512156a1d64b338b50cfa39c84f4aa}

要与第三方分析系统集成，必须侦听查看器回调，并 `trackEvent` 根据需要处 `eventInfo` 理回调函数的参数。 以下代码就是此类处理函数的示例：

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col1"> <p> <span class="codeph"> 旋转 </span> </p> </td> 
   <td colname="col2"> <p> 执行旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

