---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,User
exl-id: 34c8c7b9-0369-4d13-95f5-ad129e913453
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '67'
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

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
