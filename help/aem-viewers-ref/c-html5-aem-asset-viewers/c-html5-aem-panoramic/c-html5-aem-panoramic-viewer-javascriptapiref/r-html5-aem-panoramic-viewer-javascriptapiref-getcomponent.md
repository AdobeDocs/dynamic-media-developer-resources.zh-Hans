---
title: getComponent
description: 全景查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# getComponent{#getcomponent}

全景查看器的JavaScript API参考

`getComponent(componentId)`


返回对查看器使用的查看器SDK组件的引用。 网页可以使用此方法来扩展或自定义开箱即用查看器的行为。 仅在运行`initComplete`查看器回调后调用此方法，否则查看器逻辑可能尚未创建组件。

## 参数 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}`查看器使用的查看器SDK组件的ID。 此查看器支持以下组件ID：

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件Id </p> </th> 
   <th colname="col2" class="entry"> <p>查看器SDK组件类名称 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">容器</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">媒体集</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> panoramicView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

在使用SDK API时，请务必按照[Viewer SDK命名空间](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)中的说明使用正确的完全限定的SDK命名空间。

有关特定组件的更多信息，请参阅查看器SDK API文档。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`对查看器SDK组件的引用。 如果`componentId`不是受支持的查看器组件，或者该组件尚未由查看器逻辑创建，则此方法将返回`null`。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
