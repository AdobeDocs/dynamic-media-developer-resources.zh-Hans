---
title: ControlBar.transition
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

交互式视频查看器的配置属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持续时间`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示/隐藏控件栏及其内容的效果类型。 </p> <p>设置为<span class="codeph">无</span>可立即显示/隐藏。 </p> <p>设置为<span class="codeph">渐隐</span>以提供逐渐淡入/淡出效果。 Internet Explorer 8不支持。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">延迟隐藏</span></span> </p> </td> 
   <td colname="col2"> <p> 指定从控制栏注册的最后一个鼠标/触摸事件到控制栏隐藏之间的时间（秒）。 如果设置为<span class="codeph"> -1</span>，则组件永远不会触发其自动隐藏效果，因此将始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持续时间</span></span> </p> </td> 
   <td colname="col2"> <p> 设置淡入/淡出动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
