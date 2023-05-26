---
title: ControlBar.transition
description: 智能裁剪视频查看器的配置属性。
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

智能裁剪视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持续时间`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件栏及其内容的效果类型。 </p> <p>使用 <span class="codeph"> 无</span> 立即显示和隐藏。 使用 <span class="codeph"> 渐隐</span> 提供逐渐淡入和淡出效果。 </p> <p>Internet Explorer 8不支持渐隐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定从控制栏注册到隐藏时间控制栏的最后一个鼠标/触摸事件之间的时间（以秒为单位）。 </p> <p> 如果设置为 <span class="codeph"> -1</span>时，组件永远不会触发其自动隐藏效果，并且始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>设置淡入和淡出动画的持续时间（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
