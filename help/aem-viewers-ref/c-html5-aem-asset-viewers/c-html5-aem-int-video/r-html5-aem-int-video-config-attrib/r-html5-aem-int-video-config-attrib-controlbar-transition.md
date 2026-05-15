---
title: ControlBar.transition
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
TQID: 'https://experienceleague.adobe.com/mTLUrXKC7m8pIC5Sqoor0M-N-vmwlZzM9WxnvwzlqD8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
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

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
