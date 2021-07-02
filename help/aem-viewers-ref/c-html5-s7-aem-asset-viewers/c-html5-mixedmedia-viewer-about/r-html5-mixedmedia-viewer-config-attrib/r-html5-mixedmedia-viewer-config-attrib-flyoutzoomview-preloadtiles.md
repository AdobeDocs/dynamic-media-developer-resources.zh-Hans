---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 设置为<span class="codeph"> 1</span>可启用缩放图像的预加载。 </p> <p>设置为<span class="codeph"> 0</span>可根据需要以增量方式加载缩放图像。 </p> <p> <p>注意： 请注意，如果启用此选项，可能会显着提高带宽使用率，因为缩放的图像必须全部加载 — 即使用户没有执行缩放操作也是如此。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
