---
title: VideoPlayer.posterimage
description: 視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommand`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|[<span class="varname"> image_id</span>][？<span class="varname"> isCommand</span>]</span> </p> </td> 
   <td colname="col2"> <p> 要在視訊開始播放前的第一個影格上顯示的影像，解析針對 <span class="codeph"> serverurl</span>. 若在URL中指定，會對下列專案進行HTTP編碼： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作為 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> 和</span> 作為 <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> 作為 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果 <span class="codeph"><span class="varname"> image_id</span></span> 省略值，元件會嘗試改用該資產的預設海報影像。 </p> <p>當視訊指定為路徑時，預設海報影像目錄ID會衍生自視訊路徑，作為 <span class="codeph"> catalog_id/image_id</span> 配對： <span class="codeph"> catalog_id</span> 對應到路徑中的第一個Token。 和 <span class="codeph"> image_id</span> 是移除擴充功能的影片名稱。 如果具有該ID的影像不存在，則不會顯示海報影像。 </p> <p>若要防止顯示預設海報影像，請指定 <span class="codeph"> 無</span> 做為海報影像值。 若僅 <span class="codeph"><span class="varname"> isCommand</span></span> 指定後，會在顯示影像之前將命令套用至預設海報影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
