---
title: ControlBar.transition
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# ControlBar.transition{#controlbar-transition}

交互式视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示/隐藏控制栏及其内容的效果类型。 </p> <p>对于即时显示/隐藏，设置为<span class="codeph"> none</span>。 </p> <p>设置为<span class="codeph"> fade</span>以提供渐进渐隐/渐隐效果。 Internet Explorer 8不支持。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delayhide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制栏注册的最后一个鼠标/触摸事件与时间控制栏隐藏之间的时间（以秒为单位）。 如果设置为<span class="codeph"> -1</span>，则组件永远不会触发其自动隐藏效果，因此始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入/淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
