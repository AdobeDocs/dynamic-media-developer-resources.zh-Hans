---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: ControlBar.过渡
solution: Experience Manager
title: ControlBar.过渡
topic: Dynamic media
uuid: abd98898-d7d8-468f-b696-052e61e171b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.过渡{#controlbar-transition}

视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration(延迟`*[, *`隐藏持续时间)`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件栏及其内容的效果类型。 </p> <p>对即 <span class="codeph"> 时显示</span> 、隐藏使用“无”。 使用 <span class="codeph"> 淡入</span> 、淡出提供渐入和淡出效果。 </p> <p>Internet Explorer 8不支持淡入淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延迟隐藏</span></span> </p> </td> 
   <td colname="col2"> <p>指定控件条注册的上次鼠标／触摸事件与时间控件条隐藏的时间（以秒为单位）。 </p> <p> 如果设置为 <span class="codeph"> -1</span> ，则组件从不触发其自动隐藏效果，并始终在屏幕上保持可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 持 <span class="varname"> 续时间</span></span> </p> </td> 
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

