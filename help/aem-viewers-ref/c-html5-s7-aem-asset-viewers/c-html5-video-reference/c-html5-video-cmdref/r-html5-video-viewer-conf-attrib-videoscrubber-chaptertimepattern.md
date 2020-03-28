---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
topic: Dynamic media
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置视频章节标签标题栏中显示的时间模式，其中 <span class="codeph"> h</span> 为小时， <span class="codeph"> m为分钟，</span> s <span class="codeph"></span> 为秒。 </p> <p>用于每个时间单位的字母数确定单位要显示的数字数。 如果数字不能适合给定数字，则等效值将以后的单位显示。 </p> <p>例如，如果当前电影时间为67分5秒，则时间模式 <span class="codeph"> m:ss</span> 显示为67:05。 如果给定的时间模式为 <span class="codeph"> h:mm:s，则同一时间显示为1:07:5</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```

