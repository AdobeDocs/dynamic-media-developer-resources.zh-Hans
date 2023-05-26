---
title: 支持Adobe Analytics跟踪
description: 弹出查看器支持开箱即用的Adobe Analytics跟踪。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User,Data Engineer,Data Architect
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

弹出查看器支持开箱即用的Adobe Analytics跟踪。

## 开箱即用跟踪 {#section-ba994f079d0343c8ae48adffaa3195a3}

弹出查看器支持 [!DNL Adobe Analytics] 开箱即用跟踪。 要启用跟踪，请将相应的公司预设名称传递为 `config2` 参数。

查看器还会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须监听 `trackEvent` 查看器回调并处理 `eventInfo` 回调函数的参数（如有必要）。 以下代码是此类处理程序函数的示例：

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
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>首先加载查看器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>在查看器中交换资产时，使用 <span class="codeph"> setAsset() </span> API。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 缩放 </span> </p> </td> 
   <td colname="col2"> <p>弹出部分已激活或缩放级别已更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 平移 </span> </p> </td> 
   <td colname="col2"> <p> 图像被平移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 样本 </span> </p> </td> 
   <td colname="col2"> <p> 通过单击或点按样本可更改图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>
