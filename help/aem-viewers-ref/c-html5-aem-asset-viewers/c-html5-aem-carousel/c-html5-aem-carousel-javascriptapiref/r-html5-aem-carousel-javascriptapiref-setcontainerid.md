---
description: Carousel Viewer的JavaScript API参考。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

Carousel Viewer的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置DOM容器的ID（通常为`DIV`），查看器将插入其中。 调用此方法时不必创建容器元素。 但是，运行`init()`时必须存在容器。 必须在`init()`之前调用它。

如果将查看器配置信息与`config` JSON对象一起传递到构造函数，则此方法是可选的。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

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
