---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 设置为 <span class="codeph"> 1</span> 启用预加载缩放的图像，或将设置为 <span class="codeph"> 0</span> 以根据需要以增量方式加载缩放图像。 </p> <p> <p>注意：如果启用此选项，则可能会显着提高带宽使用率。 即使用户未启动缩放操作，缩放的图像也会全部加载。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
