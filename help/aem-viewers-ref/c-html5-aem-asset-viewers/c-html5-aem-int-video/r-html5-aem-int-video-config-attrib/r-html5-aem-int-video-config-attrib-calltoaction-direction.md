---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
uuid: fe182e8f-696d-4515-afdb-49964a374dae
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# CallToAction.direction{#calltoaction-direction}

交互式视频查看器的配置属性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|左|右  </span> </p> </td> 
   <td colname="col2"> <p> 指定缩览图填充视图的方式。 </p> <p>设置为<span class="codeph"> left </span>可设置从左到右的填充顺序。 </p> <p>设置为<span class="codeph">右</span>将颠倒顺序，以便视图以从右到左、从上到下的方向填充。 </p> <p>设置为<span class="codeph"> auto </span>以使组件在区域设置设置为<span class="codeph"> "ja" </span>时应用正确模式；否则，使用左</span>的<span class="codeph">。 </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

