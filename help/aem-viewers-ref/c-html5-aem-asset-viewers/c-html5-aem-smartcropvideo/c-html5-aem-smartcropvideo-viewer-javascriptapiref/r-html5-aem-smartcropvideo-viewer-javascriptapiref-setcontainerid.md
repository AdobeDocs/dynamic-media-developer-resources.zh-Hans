---
title: setContainerId
description: 智慧型裁切視訊檢視器的JavaScript API參考。
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

智慧型裁切視訊檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定DOM容器的ID (通常是 `DIV`)，即可將檢視器插入其中。 不需要在呼叫此方法時建立容器元素。 不過，容器必須存在於 `init()` 執行前填入。 此引數是在以下時間之前呼叫： `init()`. 如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用： `config` 建構函式的JSON物件。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 容器的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
