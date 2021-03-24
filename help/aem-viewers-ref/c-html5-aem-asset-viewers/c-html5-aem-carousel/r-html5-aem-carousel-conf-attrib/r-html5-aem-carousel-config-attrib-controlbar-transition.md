---
description: 传送查看器的配置属性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

传送查看器的配置属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控制栏及其内容的效果类型。 </p> <p>设置为<span class="codeph"> none</span>即时显示/隐藏。 </p> <p>设置为<span class="codeph">淡入/淡出</span>可提供渐进淡入/淡出效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delayhide</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制栏注册的上次鼠标/触控事件与时间控制栏隐藏之间的时间（以秒为单位）。 </p> <p>如果设置为<span class="codeph"> -1</span>，则组件从不触发其自动隐藏效果，因此始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入/淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。在禁用自动隐藏控制栏的触控设备上，将忽略此命令。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

