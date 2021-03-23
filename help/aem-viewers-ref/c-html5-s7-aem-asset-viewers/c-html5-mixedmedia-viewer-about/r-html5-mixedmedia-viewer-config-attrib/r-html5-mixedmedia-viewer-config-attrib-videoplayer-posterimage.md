---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 播放视频开始前要在第一帧上显示的图像，针对<span class="codeph"> serverurl</span>解析。 如果在URL中指定，则使用HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作 <span class="codeph"> 为%3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果省略<span class="codeph"><span class="varname"> image_id</span></span>值，则组件将尝试为该资产使用默认的海报图像。 </p> <p>当视频指定为路径时，默认的海报图像目录id从视频路径派生，因为<span class="codeph"> catalogid/imageid</span>对中<span class="codeph"> catalogid</span>对应路径中的第一个标记，而<span class="codeph"> imageid</span>是扩展名为已删除的视频的名称。 如果具有该ID的图像不存在，则不显示海报图像。 </p> <p>要阻止显示默认海报图像，请指定<span class="codeph"> none</span>作为海报图像值。 如果仅指定<span class="codeph"><span class="varname"> isCommands</span></span> ，则在显示图像之前，命令将应用于默认海报图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

无。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
