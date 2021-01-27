---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic Media
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 设置为<span class="codeph"> 1</span>以启用预加载缩放图像。 </p> <p>设置为<span class="codeph"> 0</span>可根据需要增量加载缩放图像。 </p> <p> <p>注意： 请注意，如果启用此选项，则会导致带宽使用率显着提高，因为缩放图像必须全部加载——即使用户未执行缩放操作也是如此。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
