---
title: FlyoutZoomView.fmt
description: 指定组件用于从图像服务器加载图像的图像格式。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

指定组件用于从图像服务器加载图像的图像格式。

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 如果指定的格式以 <span class="codeph"> -alpha</span>，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> <p>默认情况下，组件的背景为白色。 因此，要使其透明，请将 <span class="codeph"> 背景颜色</span> 将CSS属性设置为 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
