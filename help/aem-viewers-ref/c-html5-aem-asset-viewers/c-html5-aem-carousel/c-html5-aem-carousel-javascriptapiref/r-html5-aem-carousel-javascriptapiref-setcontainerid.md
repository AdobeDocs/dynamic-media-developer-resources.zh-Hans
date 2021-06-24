---
description: 轮播查看器的JavaScript API引用。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,Business Practitioner
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

轮播查看器的JavaScript API引用。

` setContainerId( *`containerId`*)`

设置将查看器插入其中的DOM容器的ID（通常为`DIV`）。 无需在调用此方法之前创建容器元素。 但是，运行`init()`时，容器必须存在。 必须在`init()`之前调用。

如果查看器配置信息与`config` JSON对象一起传递到构造函数，则此方法是可选的。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 容器的{ </span> string} ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
