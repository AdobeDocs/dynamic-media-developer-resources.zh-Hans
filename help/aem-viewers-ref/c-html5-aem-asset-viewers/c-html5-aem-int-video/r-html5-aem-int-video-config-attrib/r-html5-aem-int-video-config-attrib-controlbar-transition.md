---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic Media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# ControlBar.transition{#controlbar-transition}

交互式视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration(`*[, *`延迟隐藏持续时间)`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示／隐藏控件栏及其内容的效果类型。 </p> <p>设置为<span class="codeph"> none</span>即时显示／隐藏。 </p> <p>设置为<span class="codeph">淡入／淡出</span>可提供渐进淡入／淡出效果。 Internet Explorer 8不支持。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 延迟隐藏</span></span> </p> </td> 
   <td colname="col2"> <p> 指定由控制栏注册的上一个鼠标／触控事件与时间控制栏隐藏之间的时间（以秒为单位）。 如果设置为<span class="codeph"> -1</span>，则组件从不触发其自动隐藏效果，因此始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入／淡出动画的持续时间（以秒为单位）。 </p> </td> 
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

