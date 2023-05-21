---
title: setContainerId
description: 彈出式檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 5e07cbba-c1c1-4c85-af2b-ab2d84fbb709
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

彈出式檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定DOM容器的ID (通常是 `DIV`)，檢視器會插入其中。 不需要在呼叫此方法時建立容器元素。 不過，容器必須存在於 `init()` 執行前填入。 必須在之前呼叫它 `init()`. 如果透過以下方式傳遞檢視器設定資訊，則此方法為選用： `config` 建構函式的JSON物件。

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
