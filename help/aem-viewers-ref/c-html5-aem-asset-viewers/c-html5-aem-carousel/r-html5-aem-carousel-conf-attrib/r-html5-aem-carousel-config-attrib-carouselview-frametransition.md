---
description: 'null'
seo-description: 'null'
seo-title: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持续时`*[, *`间间隔`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出|幻灯片 </span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 <span class="codeph"> 没 </span> 有过渡;帧更改会立即发生。 </p> <p> <span class="codeph"> 淡 </span> 入淡出意味着新旧帧之间的交叉淡入淡出过渡。 </p> <p> <span class="codeph"> slide </span> 激活过渡，旧框架滑出视图，新框架滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 持续时 <span class="varname"></span> 间 </span> </p> </td> 
   <td colname="col2"> <p>指定淡入淡出或滑动过渡效 <span class="codeph"> 果的 </span> 持续 <span class="codeph"></span> 时间（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 间距 </span></span> </p> </td> 
   <td colname="col2"> <p>滑动过渡中相邻帧之 <span class="codeph"> 间的间 </span> 距的范围在0到 <span class="codeph"> 1之间 </span><span class="codeph"></span> ，并且相对于组件的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
