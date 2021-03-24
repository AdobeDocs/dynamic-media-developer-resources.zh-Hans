---
description: 弹出查看器支持Adobe Analytics开箱即用跟踪。
solution: Experience Manager
title: 支持Adobe Analytics跟踪
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，业务从业者，数据工程师，数据架构师
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

弹出查看器支持Adobe Analytics开箱即用跟踪。

## 现成跟踪{#section-ba994f079d0343c8ae48adffaa3195a3}

弹出查看器支持[!DNL Adobe Analytics]开箱即用跟踪。 要启用跟踪，请将正确的公司预设名称作为`config2`参数进行传递。

查看器还会向已配置的图像服务器发送单个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪{#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调并根据需要处理回调函数的`eventInfo`参数。 下面的代码就是此类处理函数的一个示例：

```
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
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>使用<span class="codeph"> setAsset()</span> API在查看器中交换资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 缩放 </span> </p> </td> 
   <td colname="col2"> <p>将激活弹出窗口或更改缩放级别。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 平移 </span> </p> </td> 
   <td colname="col2"> <p> 图像被绘制。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 样本 </span> </p> </td> 
   <td colname="col2"> <p> 通过单击或点按色板来更改图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

