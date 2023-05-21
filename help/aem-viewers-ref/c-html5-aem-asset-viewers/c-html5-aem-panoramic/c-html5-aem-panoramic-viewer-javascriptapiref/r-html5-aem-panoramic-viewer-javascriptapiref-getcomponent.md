---
title: getComponent
description: 全景檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# getComponent{#getcomponent}

全景檢視器的JavaScript API參考

`getComponent(componentId)`


傳回檢視器所使用之檢視器SDK元件的參考。 網頁可以使用此方法來延伸或自訂現成可用的檢視器的行為。 只有在下列動作之後，才呼叫此方法： `initComplete` 檢視器回呼已執行，否則檢視器邏輯可能尚未建立元件。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` 檢視器使用的Viewer SDK元件ID。 此檢視器支援下列元件ID：

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>檢視器SDK元件類別名稱 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 引數管理員 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 全景檢視 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API時，請務必使用正確的完整SDK名稱空間，如中所述 [檢視器SDK名稱空間](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

如需特定元件的詳細資訊，請參閱檢視器SDK API檔案。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器SDK元件的參考。 方法會傳回 `null` 如果 `componentId` 不是支援的檢視器元件，或是檢視器邏輯尚未建立元件。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
