---
title: 視訊時間
description: 視訊時間是顯示目前播放視訊之目前時間和持續時間的數字顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83491281-aff4-411a-a5a2-42e2454fd375
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# 視訊時間{#video-time}

視訊時間是顯示目前播放視訊之目前時間和持續時間的數字顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

視訊時間字型系列、字型大小和字型顏色是CSS可以控制的屬性。 也可以相對於包含它的控制列由CSS進行定位。

視訊時間的外觀由下列CSS類別選取器控制：

```
.s7videoviewer .s7videotime
```

## 視訊時間的CSS屬性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 視訊時間控制項的寬度。 Internet Explorer 8或更新版本需要此屬性才能正常運作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文字的字型顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

將視訊時間設為淺灰色（十六進位） `#BBBBBB`)、大小為12畫素、位置與控制列頂端的15畫素以及控制列右邊緣的80畫素。

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
