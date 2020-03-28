---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 90d36f73-44f9-4e4e-9ad6-e866749f9b2f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoTime.timepattern{#videotime-timepattern}

交互式视频查看器的配置属性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置控件栏中显示的时间模式，其中 <span class="codeph"> h表示小时</span> 、 <span class="codeph"> m</span> 表示分钟 <span class="codeph"> 、s</span> 表示秒。 </p> <p>用于每个时间单位的字母数确定单位要显示的数字数。 如果数字不能适合给定数字，则等效值将以后的单位显示。 </p> <p>例如，如果当前电影时间为67分5秒，则m:ss的时间模式 <span class="codeph"> 显示为</span> 67:05。 如果时间模式为 <span class="codeph"> h:mm:s，则同一时间显示为1:07:5</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

