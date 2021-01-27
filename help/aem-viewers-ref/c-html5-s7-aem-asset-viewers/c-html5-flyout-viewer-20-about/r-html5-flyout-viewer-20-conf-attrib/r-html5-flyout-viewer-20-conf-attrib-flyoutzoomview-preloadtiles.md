---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic Media
uuid: e73f9d5d-4b7a-4a6b-8d0f-a5e588dc00c9
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
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
   <td colname="col2"> <p> 设置为<span class="codeph"> 1</span>可启用预加载缩放图像，或设置为<span class="codeph"> 0</span>可根据需要逐步加载缩放图像。 </p> <p> <p>注意： 如果启用此选项，则可能导致带宽使用率显着提高。 缩放后的图像将全部加载，即使用户未启动缩放操作也是如此。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
