---
title: 外部视频支持
description: 查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
TQID: 'https://experienceleague.adobe.com/nLVjtwe8hj5YpMX6M1GKt1Fx-tZK2Qxe1kdWcK8BQPw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%
---
# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器既可以使用Dynamic Media Classic，也可以使用Experience Manager - Dynamic Media视频，或者使用外部视频。 如果查看器首先显示Dynamic Media Classic/Dynamic Media视频，然后将其与此类资源类型一起使用，则无法使用将外部视频加载到此查看器中 [`setVideo`]
(#reference-85d3422d6ce64a36ac74827120b5a17c)方法。 反之：如果查看器最初加载了外部视频，则它应该只处理外部视频。

处理外部视频时，查看器会忽略playback修饰符的值，并检测外部视频扩展中的播放类型。 如果外部视频URL以`.M3U8`结尾，则查看器正在使用HLS播放，否则使用渐进式播放。
