---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
TQID: 'https://experienceleague.adobe.com/bcpeaqLRZ8ClN2OulOfO9ujXzz44Yb2HTmy-GyPQ8mU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持续时间`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件栏及其内容的效果类型。 使用<span class="codeph">无</span>进行即时显示和隐藏；<span class="codeph">淡化</span>提供逐渐淡入和淡出效果（在Internet Explorer 8上不受支持）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">延迟隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定从上次注册控制栏到隐藏时间控制栏之间的时间（秒）。 </p> <p> 如果设置为<span class="codeph"> -1 </span>，则组件永远不会触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置淡入和淡出动画的持续时间（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选. 在禁用了控制栏自动隐藏的触控设备上，此命令将被忽略。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]

