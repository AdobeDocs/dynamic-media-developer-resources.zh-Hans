---
description: 轮播查看器的配置属性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

轮播查看器的配置属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控制栏及其内容的效果类型。 </p> <p>对于即时显示/隐藏，设置为<span class="codeph"> none</span>。 </p> <p>设置为<span class="codeph"> fade</span>以提供渐进渐隐/渐隐效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delayhide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制栏注册的最后一个鼠标/触摸事件与时间控制栏隐藏之间的时间（以秒为单位）。 </p> <p>如果设置为<span class="codeph"> -1</span>，则组件永远不会触发其自动隐藏效果，因此始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入/淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。在禁用控制栏自动隐藏的触控设备上，将忽略此命令。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
