---
title: ControlBar.transition
description: 轮播查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

轮播查看器的配置属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`持续时间`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件栏及其内容的效果类型。 </p> <p>设置为 <span class="codeph"> 无</span> 用于即时显示/隐藏。 </p> <p>设置为 <span class="codeph"> 渐隐</span> 提供逐渐淡入/淡出效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定从控制栏注册的上一个鼠标/触摸事件到控制栏隐藏的时间（以秒为单位）。 </p> <p>如果设置为 <span class="codeph"> -1</span> 组件从不触发其自动隐藏效果，因此始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入/淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选. 在禁用了控制栏自动隐藏的触控设备上，此命令将被忽略。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
