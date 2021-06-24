---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,Business Practitioner
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 设置为<span class="codeph"> 1</span>可启用缩放图像的预加载，或设置为<span class="codeph"> 0</span>可根据需要以增量方式加载缩放图像。 </p> <p> <p>注意： 如果启用此选项，则可能会显着提高带宽使用率。 即使用户未启动缩放操作，缩放的图像也会全部加载。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
