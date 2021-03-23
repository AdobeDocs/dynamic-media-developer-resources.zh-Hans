---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: e48b39bb-c23d-42ce-9dc6-6e8b0d9b04ea
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 </p> <p> 当设置为<span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>或<span class="codeph"> right </span>时，面板将沿指定方向滚出，而不进行额外的边界检查。 此行为可能导致外部容器剪切面板。 </p> <p>当设置为<span class="codeph"> fit-vertical </span>时，组件会首先将基面板位置移到SocialShare的底部，并尝试从底部、右侧或左侧从此基本位置展开面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基板位置移到顶部，并从顶部、右侧和左侧重复滚出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral </span>时，组件使用与fit-vertical类似的逻辑，而是将基座向右首先、向下和向上滚动方向移动，然后将基座向左移动，尝试向左、向下和向上滚动方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8e843b967237426e9a8b3cd0f27b9820}

可选。

## 默认 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 示例 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
