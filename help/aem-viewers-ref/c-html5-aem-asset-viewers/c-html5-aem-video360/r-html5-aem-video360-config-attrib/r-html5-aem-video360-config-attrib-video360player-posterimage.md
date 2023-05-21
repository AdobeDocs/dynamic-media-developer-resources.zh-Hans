---
title: Video360Player.posterimage
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 11%

---

# Video360Player.posterimage{#video-player-posterimage}

Video360 Viewer的設定屬性。

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommand`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommand</span>]</span> </p> </td> 
   <td colname="col2"> <p> 影像伺服修飾元，可控制海報影像外觀。 若在URL中指定，會對下列專案進行HTTP編碼： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作為 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> 和</span> 作為 <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> 作為 <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> 此修飾詞適用於Dynamic Media Classic或Adobe Experience Manager、Dynamic Media上託管的視訊內容。 </p> <p>若要防止顯示預設海報影像，請指定 <span class="codeph"> 無</span> 做為海報影像值。 </p> </td> 
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
