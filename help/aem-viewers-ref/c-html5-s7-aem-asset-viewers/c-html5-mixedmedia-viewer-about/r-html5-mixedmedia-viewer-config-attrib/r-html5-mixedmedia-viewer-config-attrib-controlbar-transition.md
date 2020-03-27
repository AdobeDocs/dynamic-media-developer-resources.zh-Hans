---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.过渡
solution: Experience Manager
title: ControlBar.过渡
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.过渡{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration(延迟`*[, *`隐藏持续时间)`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
