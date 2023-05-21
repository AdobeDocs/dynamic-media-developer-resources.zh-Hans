---
title: ControlBar.transition
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

互動式視訊檢視器的設定屬性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持續時間`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> 指定用來顯示/隱藏控制列及其內容的效果型別。 </p> <p>設定為 <span class="codeph"> 無</span> 立即顯示/隱藏。 </p> <p>設定為 <span class="codeph"> 淡化</span> 提供逐漸淡入/淡出效果。 Internet Explorer 8不支援。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定控制列註冊的上一個滑鼠/觸控事件與控制列隱藏時間之間的時間（以秒為單位）。 若設為 <span class="codeph"> -1</span> 元件不會觸發其自動隱藏效果，因此一律會顯示在熒幕上。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 設定淡入/淡出動畫的持續時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
