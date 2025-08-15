---
title: CallToAction.direction
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

交互式视频查看器的配置属性。

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|左|右</span> </p> </td> 
   <td colname="col2"> <p> 指定缩略图在视图中填充的方式。 </p> <p>设置为左<span class="codeph">的</span>以设置从左至右的填充顺序。 </p> <p>设置为<span class="codeph">右</span>将颠倒顺序，以便视图按从右至左、从上至下的方向填充。 </p> <p>设置为<span class="codeph">自动</span>可在区域设置设置为<span class="codeph">“ja”</span>时使组件应用右模式；否则，将使用<span class="codeph">左</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
