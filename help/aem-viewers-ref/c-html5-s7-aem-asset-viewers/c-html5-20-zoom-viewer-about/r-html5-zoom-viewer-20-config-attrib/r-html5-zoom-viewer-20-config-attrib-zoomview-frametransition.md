---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: Developer,Business Practitioner
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`持续时间间距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐|幻灯片  </span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 <span class="codeph"> “无” </span> 表示不表示任何过渡；帧更改会立即发生。<span class="codeph"> 淡 </span> 入色是指在旧帧和新帧之间进行交叉淡入色过渡。<span class="codeph"> slide </span> 可激活以下过渡：旧框架滑出视图，而新框架滑入视图。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间  </span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">渐隐</span>或<span class="codeph">幻灯片</span>过渡效果的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 间距  </span> </span> </p> </td> 
   <td colname="col2"> <p>在<span class="codeph">滑动</span>过渡中相邻帧之间的间距在<span class="codeph"> 0 </span>和<span class="codeph"> 1 </span>之间，并且相对于组件的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
