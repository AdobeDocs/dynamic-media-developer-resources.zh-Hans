---
title: VideoPlayer.singleclick
description: VideoPlayer.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2ec6d871-05d9-4d85-b031-e64386f5d2e9
TQID: 'https://experienceleague.adobe.com/5M4n9Fv-9s7q525GnTPpHcykVnDaVwudvjctOjG-kNg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`无|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按到切换播放/暂停的映射。 设置为<span class="codeph"> none</span>可禁用通过单击/点按进行播放/暂停的功能。 如果设置为<span class="codeph"> playPause</span>，则单击视频可在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在这种情况下，<span class="codeph"> singleclick</span>行为已禁用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
