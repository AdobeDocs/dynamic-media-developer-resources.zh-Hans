---
description: eCatalog搜索查看器支持开箱即用的Adobe Analytics跟踪。
solution: Experience Manager
title: 支持Adobe Analytics跟踪
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 支持Adobe Analytics跟踪{#support-for-adobe-analytics-tracking}

eCatalog搜索查看器支持开箱即用的Adobe Analytics跟踪。

## 开箱即用跟踪 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog搜索查看器支持[!DNL Adobe Analytics]开箱即用跟踪。 要启用跟踪，请将适当的公司预设名称作为`config2`参数传递。

查看器还会向配置的图像服务器发送一个跟踪HTTP请求，其中包含查看器类型和版本信息。

## 自定义跟踪 {#section-cda48fc9730142d0bb3326bac7df3271}

要与第三方分析系统集成，必须侦听`trackEvent`查看器回调，并根据需要处理回调函数的`eventInfo`参数。 以下代码是此类处理程序函数的示例：

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph">页</span> </p> </td> 
   <td colname="col2"> <p> 当前帧将在主视图中更改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">项</span> </p> </td> 
   <td colname="col2"> <p>激活信息面板弹出窗口。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>由于单击图像映射，用户导航到其他页面。 </p> </td> 
  </tr> 
 </tbody> 
</table>
