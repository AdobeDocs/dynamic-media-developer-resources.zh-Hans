---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: InteractiveSwatches.direction
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

交互式视频查看器的配置属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|左|右  </span> </p> </td> 
   <td colname="col2"> <p> 指定色板填充视图的方式。 </p> <p>设置为<span class="codeph"> left </span>可设置从左到右的填充顺序。 </p> <p>设置为<span class="codeph">右</span>将颠倒顺序，以便视图以从右到左、从上到下的方向填充。 </p> <p>设置<span class="codeph">自动</span>时，当区域设置设置为" <span class="codeph"> ja </span>"时，组件将应用正确模式；否则，使用左</span>的<span class="codeph">。 </span></p> </td> 
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
