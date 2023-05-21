---
title: ControlBar.transition
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7b4db11b-e9ac-4a52-9206-083989128bc6
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

智慧型裁切視訊檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示或隱藏控制列及其內容的效果型別。 </p> <p>使用 <span class="codeph"> 無</span> 以立即顯示和隱藏。 使用 <span class="codeph"> 淡化</span> 提供逐漸淡入和淡出效果。 </p> <p>Internet Explorer 8不支援淡化。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制列註冊的最後一個滑鼠/觸控事件與控制列隱藏的時間之間的時間（以秒為單位）。 </p> <p> 若設為 <span class="codeph"> -1</span>，元件絕不會觸發其自動隱藏效果，且一律會顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入和淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
