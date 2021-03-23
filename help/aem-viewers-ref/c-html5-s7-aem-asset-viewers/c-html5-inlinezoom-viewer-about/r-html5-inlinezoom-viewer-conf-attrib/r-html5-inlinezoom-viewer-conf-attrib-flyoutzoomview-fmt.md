---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
uuid: 570a9cca-17fa-44d5-b3bb-66ec19453cbc
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> <p>请注意，默认情况下，组件的背景为白色。 因此，要使其完全透明，请将<span class="codeph"> background-color</span> CSS属性设置为<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
