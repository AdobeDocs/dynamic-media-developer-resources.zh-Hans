---
description: Video360查看器的配置属性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Video360查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控制栏及其内容的效果类型。 </p> <p>使用<span class="codeph"> none</span>进行即时显示和隐藏。 使用<span class="codeph">淡入和淡出效果。</span> </p> <p>Internet Explorer 8不支持淡入淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delayhide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制栏注册的上次鼠标/触摸事件与时间控制栏隐藏的时间（以秒为单位）。 </p> <p> 如果设置为<span class="codeph"> -1</span>，则组件从不触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>设置淡入和淡出动画的持续时间（以秒为单位）。 </p> </td> 
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
