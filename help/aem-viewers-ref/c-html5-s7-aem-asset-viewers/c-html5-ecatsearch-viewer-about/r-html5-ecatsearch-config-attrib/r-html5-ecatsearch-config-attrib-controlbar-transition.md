---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic Media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration(`*[, *`延迟隐藏持续时间)`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出  </span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件条及其内容的效果类型。 使用<span class="codeph"> none </span>进行即时显示和隐藏；<span class="codeph">淡入淡出</span>提供渐进淡出和淡出效果（Internet Explorer 8不支持）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延迟隐藏  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制栏注册的上次鼠标／触控事件与时间控制栏隐藏的时间（以秒为单位）。 </p> <p> 如果设置为<span class="codeph"> -1 </span>，则组件从不触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间  </span> </span> </p> </td> 
   <td colname="col2"> <p> 设置动画淡入和淡出的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。在触控设备上忽略此命令，其中禁用了控制栏自动隐藏。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
