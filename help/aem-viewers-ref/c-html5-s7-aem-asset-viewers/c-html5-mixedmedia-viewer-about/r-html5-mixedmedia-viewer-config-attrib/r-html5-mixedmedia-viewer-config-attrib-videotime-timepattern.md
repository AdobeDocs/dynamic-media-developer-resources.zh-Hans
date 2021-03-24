---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置在控制栏中显示的时间模式，其中<span class="codeph"> h</span>为小时，<span class="codeph"> m</span>为分钟，<span class="codeph"> s</span>为秒。 </p> <p>每个时间单位使用的字母数决定单位要显示的数字数。 如果数字不能容纳给定数字，则在后续单位中显示等效值。 </p> <p>例如，如果当前电影时间为67分5秒，则时间模式<span class="codeph"> m:ss</span>显示为67:05。 如果给定的时间模式为<span class="codeph"> h:mm:s</span>，则同一时间显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
