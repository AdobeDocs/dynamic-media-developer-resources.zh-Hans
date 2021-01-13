---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: 302e20bf-d398-45de-98a5-58b9edde48f3
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件将图像视为不透明。 默认情况下，该组件具有白色背景。 因此，要使其透明，请将<span class="codeph"> background-color</span> CSS属性设置为<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

可选。

## 默认 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 示例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
