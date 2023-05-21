---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示或隱藏控制列及其內容的效果型別。 使用 <span class="codeph"> 無 </span> 即時顯示和隱藏； <span class="codeph"> 淡化 </span> 提供逐漸淡入和淡出效果（Internet Explorer 8不支援）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制列註冊的最後一個滑鼠/觸控事件與控制列隱藏的時間之間的時間（以秒為單位）。 </p> <p> 若設為 <span class="codeph"> -1 </span> 元件絕不會觸發其自動隱藏效果，且一律顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定淡入和淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选. 在觸控裝置上，這個指令會被忽略，因為控制列自動隱藏已停用。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
