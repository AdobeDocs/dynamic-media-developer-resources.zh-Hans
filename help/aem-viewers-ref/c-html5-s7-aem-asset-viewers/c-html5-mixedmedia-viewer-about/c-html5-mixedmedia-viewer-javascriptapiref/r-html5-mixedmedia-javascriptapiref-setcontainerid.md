---
description: 混合媒体查看器的JavaScript API引用。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

混合媒体查看器的JavaScript API引用。

` setContainerId( *`containerId`*)`

设置将查看器插入其中的DOM容器（通常是DIV）的ID。 无需在调用此方法之前创建容器元素。 但是，运行`init()`时，容器必须存在。 必须在`init()`之前调用。 如果查看器配置信息与`config` JSON对象一起传递到构造函数，则此方法是可选的。

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
