---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`持续时间`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定用于显示或隐藏控件栏及其内容的效果类型。 </p> <p>使用<span class="codeph"> none</span>进行即时显示和隐藏。 使用<span class="codeph"> fade</span>提供逐渐淡入和淡出效果。 </p> <p>Internet Explorer 8不支持渐隐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>指定从上次注册控制栏的鼠标/触摸事件到隐藏控制栏的时间（秒）。 </p> <p> 如果设置为<span class="codeph"> -1</span>，则组件永远不会触发其自动隐藏效果，并始终在屏幕上可见。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>设置淡入和淡出动画的持续时间（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
