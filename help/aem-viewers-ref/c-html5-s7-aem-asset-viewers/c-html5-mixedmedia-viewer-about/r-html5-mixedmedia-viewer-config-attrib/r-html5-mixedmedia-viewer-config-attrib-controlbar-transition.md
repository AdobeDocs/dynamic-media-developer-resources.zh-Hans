---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示或隱藏控制列及其內容的效果型別。 </p> <p>使用 <span class="codeph"> 無</span> 以立即顯示和隱藏。 使用 <span class="codeph"> 淡化</span> 提供逐漸淡入和淡出效果。 </p> <p>Internet Explorer 8不支援淡化。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制列註冊的上次滑鼠/觸控事件與控制列隱藏時間之間的時間（以秒為單位）。 </p> <p> 若設為 <span class="codeph"> -1</span>，元件絕不會觸發其自動隱藏效果，且一律會顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間</span> </span> </p> </td> 
   <td colname="col2"> <p>設定淡入和淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
