---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.bearding
solution: Experience Manager
title: SocialShare.bearding
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SocialShare.bearding{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 </p> <p> 当设置为向上 <span class="codeph"> 、向下 </span>或向左 <span class="codeph"> 向上时， </span><span class="codeph"></span><span class="codeph"></span>面板将沿指定方向滚出，而不进行额外的边界检查。 此行为可能导致面板被外部容器裁切。 </p> <p>当设置为 <span class="codeph"> 适合垂直 </span>时，组件首先将基板位置移至SocialShare的底部，并尝试从底部、右侧或左侧从此基本位置展开面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试均失败，则组件会尝试将基板位置移到顶部，并重复从顶部、右侧和左侧的滚出尝试。 </p> <p>当设置为 <span class="codeph"></span>fit-lateral时，该组件使用与fit-vertical类似的逻辑，而是将基座移向右首尝试右、下和上滚出方向——然后将基座移向左、尝试左、下和上滚出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8e843b967237426e9a8b3cd0f27b9820}

可选。

## 默认 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 示例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
