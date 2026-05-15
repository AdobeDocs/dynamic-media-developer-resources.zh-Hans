---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
TQID: 'https://experienceleague.adobe.com/65cLC5DOqdGrbVpMMy6gLBNL4F3WRqipNqIlpBIK-GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`持续时间`*[, *`间距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|渐隐|幻灯片</span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 例如，<span class="codeph"> none </span>表示无过渡；帧更改会立即发生。 并且， </p> <p> <span class="codeph">渐隐</span>表示旧帧和新帧之间的交叉渐隐过渡。 最后， </p> <p> <span class="codeph">幻灯片</span>激活旧框架滑出视图和新框架滑入的过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>指定<span class="codeph">渐隐</span>或<span class="codeph">幻灯片</span>过渡效果的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">间距</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">幻灯片</span>过渡中相邻帧之间的间距范围介于<span class="codeph"> 0 </span>到<span class="codeph"> 1 </span>之间，并且与组件的宽度相关。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
