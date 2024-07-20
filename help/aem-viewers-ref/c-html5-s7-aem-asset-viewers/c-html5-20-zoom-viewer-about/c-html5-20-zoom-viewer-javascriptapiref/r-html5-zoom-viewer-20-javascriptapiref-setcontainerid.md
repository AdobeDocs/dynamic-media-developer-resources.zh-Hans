---
title: setContainerId
description: 视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 87f01c5f-0d2a-46d6-8026-e75e879532df
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

视频查看器的JavaScript API参考。

` setContainerId( *`containerId`*)`

设置查看器插入到的DOM容器（通常是DIV）的ID。 在调用此方法时，无需创建容器元素。 但是，运行`init()`时容器必须存在。 必须在`init()`之前调用它。

如果将查看器配置信息与`config` JSON对象一起传递给构造函数，则此方法是可选的。

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
