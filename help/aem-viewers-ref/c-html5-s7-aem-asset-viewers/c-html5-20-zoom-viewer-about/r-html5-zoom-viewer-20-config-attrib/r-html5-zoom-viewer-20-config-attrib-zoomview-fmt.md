---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic media
uuid: 8e3e16a8-7b3c-4cb0-9c6d-a067bc7f6191
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 如果指定的格式以 <span class="codeph"> -alpha结尾</span>，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件将图像视为不透明。 默认情况下，该组件具有白色背景。 因此，要使其透明，请将 <span class="codeph"> background-color</span> CSS属性设置为 <span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
