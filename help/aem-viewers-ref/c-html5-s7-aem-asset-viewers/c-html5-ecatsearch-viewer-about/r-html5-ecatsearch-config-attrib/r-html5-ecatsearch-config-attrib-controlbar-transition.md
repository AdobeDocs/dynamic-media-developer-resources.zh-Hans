---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无  </span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控制栏及其内容的效果类型。 使用<span class="codeph"> none </span>进行即时显示和隐藏；<span class="codeph"> fade </span>提供渐进淡入和淡出效果（Internet Explorer 8不支持）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delayhide  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定控制栏注册的上次鼠标/触摸事件与时间控制栏隐藏的时间（以秒为单位）。 </p> <p> 如果设置为<span class="codeph"> -1 </span>，则组件从不触发其自动隐藏效果，并始终在屏幕上显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间  </span> </span> </p> </td> 
   <td colname="col2"> <p> 设置淡入和淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。在触控设备上，此命令会被忽略，此时会禁用控制栏自动隐藏。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
