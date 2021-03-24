---
description: CarouselView.fmt
solution: Experience Manager
title: CarouselView.fmt
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---


# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 </p> <p>如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 </p> <p>对于所有其他图像格式，组件会将图像视为不透明。 默认情况下，该组件的背景为白色。 因此，要使其透明，请将<span class="codeph"> background-color</span> CSS属性设置为<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
