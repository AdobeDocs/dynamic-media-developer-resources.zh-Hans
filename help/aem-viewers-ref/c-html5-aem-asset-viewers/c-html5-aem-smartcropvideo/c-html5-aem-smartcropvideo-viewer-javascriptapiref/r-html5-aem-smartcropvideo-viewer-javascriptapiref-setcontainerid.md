---
description: 智能裁剪视频查看器的JavaScript API引用。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

智能裁剪视频查看器的JavaScript API引用。

` setContainerId( *`containerId`*)`

设置DOM容器的ID(通常为 `DIV`)，将查看器插入到其中。 无需在调用此方法之前创建容器元素。 但是，容器必须存在于 `init()` 运行。 此参数在 `init()`. 如果查看器配置信息是通过 `config` 构造函数的JSON对象。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
