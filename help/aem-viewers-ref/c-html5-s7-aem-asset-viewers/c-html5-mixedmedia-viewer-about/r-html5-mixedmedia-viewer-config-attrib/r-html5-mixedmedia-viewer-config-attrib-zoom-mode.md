---
description: 设置缩放交互的类型。
seo-description: 设置缩放交互的类型。
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 2%

---


# zoomMode{#zoommode}

设置缩放交互的类型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 连续|内联|自动  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous可 </span> 在主视图中单击、多次点按或捏合缩小图像时逐渐放大的经典缩放功能。您需要显式缩小或重置缩放状态，才能返回到初始视图。 </p> <p> <span class="codeph"> 内联 </span> 支持即时缩放，当您将主视图悬停在桌面上或在触控设备上触控时，缩放后的图像会立即显示；当您将鼠标从视图移开或松开手指时，图像会自动还原为初始状态。请注意，在内嵌</span>模式中，嵌套图像集是拼合的，并以单个缩览图的形式显示。 <span class="codeph"><span class="codeph"> 在桌 </span> 面上自动激活内联模式，在触控设备上自动激活连续模式。 </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
