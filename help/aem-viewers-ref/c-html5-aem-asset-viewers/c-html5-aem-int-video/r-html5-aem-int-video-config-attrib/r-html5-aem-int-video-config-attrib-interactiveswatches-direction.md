---
title: InteractiveSwatches.direction
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
TQID: 'https://experienceleague.adobe.com/Rl1O2CZOwu8Fp9kNIrHIGV2Ef09ssznrrrRV5J3-Gfc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 3%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

交互式视频查看器的配置属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|左|右</span> </p> </td> 
   <td colname="col2"> <p> 指定样本在视图中填充的方式。 </p> <p>设置为左</span>的<span class="codeph">以设置从左至右的填充顺序。 </p> <p>设置为<span class="codeph">右</span>将颠倒顺序，以便视图按从右至左、从上至下的方向填充。 </p> <p>当设置了<span class="codeph">自动</span>时，组件在区域设置设置为“<span class="codeph"> ja </span>”时应用右模式；否则，使用<span class="codeph">左侧</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
