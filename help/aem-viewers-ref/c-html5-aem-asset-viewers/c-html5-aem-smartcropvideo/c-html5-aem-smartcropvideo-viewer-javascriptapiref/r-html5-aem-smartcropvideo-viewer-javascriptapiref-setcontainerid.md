---
title: setContainerId
description: 智能裁剪视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 1c7a7494-e872-4e78-9518-ea30af46303c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

智能裁剪视频查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置查看器插入的DOM容器的ID（通常为`DIV`）。 在调用此方法时，无需创建容器元素。 但是，运行`init()`时容器必须存在。 此参数在`init()`之前调用。 如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> 容器的<span class="codeph"> {string} </span> ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
