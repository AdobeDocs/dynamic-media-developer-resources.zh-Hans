---
description: Video Viewer的JavaScript API参考。
seo-description: Video Viewer的JavaScript API参考。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
uuid: a4b741a1-b0b3-4bc3-aeab-9d0e44ec4e79
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# setContainerId{#setcontainerid}

Video Viewer的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置查看器插入的DOM容器的ID（通常为`DIV`）。 调用此方法时不必创建容器元素。 但是，运行`init()`时必须存在容器。 此参数在`init()`之前调用。 如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

