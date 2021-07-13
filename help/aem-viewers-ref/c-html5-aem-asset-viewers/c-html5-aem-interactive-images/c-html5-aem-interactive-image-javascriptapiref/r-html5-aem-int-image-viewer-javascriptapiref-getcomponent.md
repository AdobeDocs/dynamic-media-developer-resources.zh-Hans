---
description: 视频图像查看器的JavaScript API引用。
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,User
exl-id: 5f2514a9-bbd0-436d-ad96-b89778604f8a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---

# getComponent{#getcomponent}

视频图像查看器的JavaScript API引用。

`getComponent(componentId)`

返回对查看器所使用的查看器SDK组件的引用。 网页可以使用此方法来扩展或自定义现成查看器的行为。 仅在运行`initComplete`查看器回调后才调用此方法，否则查看器逻辑可能尚未创建该组件。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  -  `{String}` 查看器使用的查看器SDK组件的ID。此查看器支持以下组件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件ID </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK组件类名称 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API时，务必使用正确的完全限定SDK命名空间，如[查看器SDK命名空间](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265)中所述。

有关特定组件的更多信息，请参阅查看器SDK API文档。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器SDK组件的引用。如果`componentId`不是受支持的查看器组件，或者查看器逻辑尚未创建该组件，则方法会返回`null`。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
