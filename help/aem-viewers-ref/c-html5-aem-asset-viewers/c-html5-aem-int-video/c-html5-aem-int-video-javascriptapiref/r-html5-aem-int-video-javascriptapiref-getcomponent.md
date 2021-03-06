---
title: getComponent
description: 交互式视频查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a760bc86-b700-4ffe-9983-ef55d88677d6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# getComponent{#getcomponent}

交互式视频查看器的JavaScript API引用。

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
   <td colname="col1"> <p> <span class="codeph"> videoPlayer  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> interactiveSwatches  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.InteractiveSwatches  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> callToAction  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CallToAction  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closedCaptionButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 控件 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API时，务必使用正确且完全限定的SDK命名空间，如[查看器SDK命名空间](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-html5-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)中所述。

有关特定组件的更多信息，请参阅&#x200B;*查看器SDK API*&#x200B;文档。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器SDK组件的引用。如果`componentId`不是受支持的查看器组件，或者查看器逻辑尚未创建该组件，则方法会返回`null`。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
} 
})
```
