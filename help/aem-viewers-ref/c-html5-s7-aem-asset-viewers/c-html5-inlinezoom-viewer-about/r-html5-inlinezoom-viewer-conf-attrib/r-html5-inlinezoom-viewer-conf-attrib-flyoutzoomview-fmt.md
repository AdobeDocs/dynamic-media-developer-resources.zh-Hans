---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件从图像服务器加载图像时使用的图像格式。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> <p>默认情况下，该组件具有白色背景。 因此，若要使其透明，请将<span class="codeph"> background-color</span> CSS属性设置为<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
