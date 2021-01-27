---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic Media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`持续`*[, *`间距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出|幻灯片  </span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 <span class="codeph"> “无 </span> ”表示没有过渡；帧更改会立即发生。<span class="codeph"> 淡 </span> 入淡出意味着新旧帧之间的交叉淡入淡出过渡。<span class="codeph"> 幻灯 </span> 片可激活旧框架滑出视图和新框架滑入的过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间  </span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">淡入淡出</span>或<span class="codeph">幻灯片</span>过渡效果的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 间距  </span> </span> </p> </td> 
   <td colname="col2"> <p>在<span class="codeph">幻灯片</span>过渡中相邻帧之间的间距具有<span class="codeph"> 0 </span>和<span class="codeph"> 1 </span>之间的范围，并且与组件的宽度相关。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
