---
title: InteractiveSwatches.direction
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

交互式视频查看器的配置属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|左|右  </span> </p> </td> 
   <td colname="col2"> <p> 指定色板在视图中的填充方式。 </p> <p>将设置为左</span>的<span class="codeph">以设置从左到右的填充顺序。 </span></p> <p>设置为<span class="codeph">右</span>可反转顺序，以便视图以从右到左、从上到下的方向填充。 </p> <p>设置<span class="codeph">自动</span>后，当区域设置设置为“ <span class="codeph"> ja </span>”时，组件会应用正确模式；否则，使用左</span>的<span class="codeph">。 </span></p> </td> 
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
