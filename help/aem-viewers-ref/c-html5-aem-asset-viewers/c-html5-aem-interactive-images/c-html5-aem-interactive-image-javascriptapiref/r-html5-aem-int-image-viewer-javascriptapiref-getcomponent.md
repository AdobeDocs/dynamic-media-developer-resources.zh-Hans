---
description: Video Image Viewer的JavaScript API参考。
seo-description: Video Image Viewer的JavaScript API参考。
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 6dd112f1-7b34-4d04-969e-b0cef46b4ad4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# getComponent{#getcomponent}

Video Image Viewer的JavaScript API参考。

`getComponent(componentId)`

返回对查看器使用的查看器SDK组件的引用。 网页可以使用此方法扩展或自定义现成查看器的行为。 只有在`initComplete`查看器回调运行后才调用此方法，否则查看器逻辑可能尚未创建该组件。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  - `{String}` 查看器使用的查看器SDK组件的ID。此查看器支持以下组件ID:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件ID </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK组件类名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 参数管理器  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.容器  </span> </p> </td> 
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

使用SDK API时，务必使用[查看器SDK命名空间](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265)中所述的正确完全限定的SDK命名空间。

有关特定组件的更多信息，请参阅查看器SDK API文档。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器SDK组件的引用。如果`componentId`不是支持的查看器组件，或者查看器逻辑尚未创建该组件，则此方法返回`null`。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

