---
description: 播放图标会覆盖在主视图区域上。 它在暂停视频或到达视频末尾时显示，还取决于iconeffect参数。
seo-description: 播放图标会覆盖在主视图区域上。 它在暂停视频或到达视频末尾时显示，还取决于iconeffect参数。
seo-title: 图标效果
solution: Experience Manager
title: 图标效果
uuid: 81c9c344-5256-4015-8d02-abbf09dca541
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# 图标效果{#icon-effect}

播放图标会覆盖在主视图区域上。 它在暂停视频或到达视频末尾时显示，还取决于iconeffect参数。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放图标的外观由以下CSS类选择器控制：

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
```

**播放图标的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 播放图标的显示图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 播放图标的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>播放图标的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

图标效果支持`state`属性选择器。 `state="play"` 当视频在播放中间暂停时使用，当播 `state="replay"` 放头在流的末尾时使用。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

设置100 x 100像素播放图标。

```
.s7interactivevideoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

