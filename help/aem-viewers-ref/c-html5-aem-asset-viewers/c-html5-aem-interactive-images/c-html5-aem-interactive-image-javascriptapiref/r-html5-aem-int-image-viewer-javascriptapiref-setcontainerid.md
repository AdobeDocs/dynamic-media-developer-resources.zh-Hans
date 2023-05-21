---
title: setContainerId
description: 影片影像檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 2b9b89e6-50ea-458f-9da2-6fda1884935c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

影片影像檢視器的JavaScript API參考。

` setContainerId( *`containerId`*)`

設定檢視器插入其中的DOM容器（通常是DIV）的ID。 不需要在呼叫此方法時建立容器元素。 不過，容器必須存在於 `init()` 執行前填入。 必須在之前呼叫它 `init()`.

如果檢視器組態資訊是透過以下方式傳遞，則此方法為選用 `config` 建構函式的JSON物件。

## 参数 {#section-fa807db629ce43bab286b1e1dc96c492}

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
