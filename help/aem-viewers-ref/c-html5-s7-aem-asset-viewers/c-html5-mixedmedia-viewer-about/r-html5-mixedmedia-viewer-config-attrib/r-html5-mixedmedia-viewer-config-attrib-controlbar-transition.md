---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic Media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration(`*[, *`延迟隐藏持续时间)`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件条及其内容的效果类型。 </p> <p>使用<span class="codeph"> none</span>进行即时显示和隐藏。 使用<span class="codeph">淡入淡出</span>提供渐入淡出效果。 </p> <p>Internet Explorer 8不支持淡入淡出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 延迟隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p>指定控制栏注册的上次鼠标／触控事件与时间控制栏隐藏的时间（以秒为单位）。 </p> <p> 如果设置为<span class="codeph"> -1</span>，则组件从不触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>设置动画淡入和淡出的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
