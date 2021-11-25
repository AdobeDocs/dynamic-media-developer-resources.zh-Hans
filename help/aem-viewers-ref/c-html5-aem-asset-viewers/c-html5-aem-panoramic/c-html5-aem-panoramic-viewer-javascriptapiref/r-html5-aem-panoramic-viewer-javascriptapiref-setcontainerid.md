---
title: setContainerId
description: 全景查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

全景查看器的JavaScript API引用。

` setContainerId( *`containerId`*)`

设置将查看器插入其中的DOM容器（通常是DIV）的ID。 无需在调用此方法之前创建容器元素。 但是，容器必须存在于 `init()` 运行。 必须在 `init()`.

如果查看器配置信息与 `config` 构造函数的JSON对象。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

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
