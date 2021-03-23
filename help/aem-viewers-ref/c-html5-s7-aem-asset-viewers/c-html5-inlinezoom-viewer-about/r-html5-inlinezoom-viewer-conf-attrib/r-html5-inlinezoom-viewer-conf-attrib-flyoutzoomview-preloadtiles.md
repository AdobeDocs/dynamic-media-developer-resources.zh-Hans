---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: 8e989ca7-1ef7-4758-b6b9-c447d7647d1d
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 设置为<span class="codeph"> 1</span>可启用预加载缩放图像，或设置为<span class="codeph"> 0</span>可根据需要逐步加载缩放图像。 </p> <p> <p>注意： 如果启用此选项，则会显着提高带宽使用率。 即使用户未启动缩放操作，缩放的图像也会全部加载。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
