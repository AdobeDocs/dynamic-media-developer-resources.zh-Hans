---
title: Video360Player.posterimage
description: Video360 Viewer的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
TQID: 'https://experienceleague.adobe.com/LtpJ2MbHJ038-dI9WI-b3XUoVoxx2OG11SbAupux-BI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 5%

---

# Video360Player.posterimage{#video-player-posterimage}

Video360 Viewer的配置属性。

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|[？<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制海报图像外观的图像服务修饰符。 如果在URL中指定，则对以下内容进行HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作为<span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span>作为<span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span>作为<span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> 此修饰符适用于Dynamic Media Classic或Adobe Experience Manager、Dynamic Media上托管的视频内容。 </p> <p>要阻止显示默认海报图像，请将<span class="codeph"> none</span>指定为海报图像值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
