---
title: 支持Adobe Analytics跟踪
description: 支持Adobe Analytics跟踪
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

默认情况下，查看器会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须监听 `trackEvent` 查看器回调和处理 `eventInfo` 回调函数的参数（如有必要）。 以下代码是此类处理程序函数的示例：

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>已发送... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>首次加载查看器时。 </p> </td> 
  </tr> 
 </tbody> 
</table>
