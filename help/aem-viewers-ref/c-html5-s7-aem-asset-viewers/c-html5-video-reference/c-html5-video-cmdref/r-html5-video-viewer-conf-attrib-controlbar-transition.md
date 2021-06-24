---
description: 视频查看器的配置属性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,Business Practitioner
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控制栏及其内容的效果类型。 </p> <p>使用<span class="codeph"> none</span>进行即时显示和隐藏。 使用<span class="codeph"> fade</span>提供渐进渐隐和渐隐效果。 </p> <p>Internet Explorer 8不支持渐隐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delayhide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制栏注册的上次鼠标/触摸事件与时间控制栏隐藏之间的时间（以秒为单位）。 </p> <p> 如果设置为<span class="codeph"> -1</span>，则组件永远不会触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>设置动画淡入和淡出的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
