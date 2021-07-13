---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`持续时间间距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐|幻灯片  </span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 <span class="codeph"> 没 </span> 有代表过渡；帧更改会立即发生。 </p> <p> <span class="codeph"> 淡 </span> 入色是指在旧帧和新帧之间进行交叉淡入色过渡。 </p> <p> <span class="codeph"> slide </span> 可激活以下过渡：旧框架滑出视图，而新框架滑入视图。 </p> </td> 
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

`frametransition=fade,0.3`
