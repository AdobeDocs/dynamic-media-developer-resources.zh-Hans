---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 </p> <p> 当设置为<span class="codeph"> up </span>、<span class="codeph"> down </span>、<span class="codeph"> left </span>或<span class="codeph"> right </span>时，面板将按指定方向滚出，而无需额外的范围检查。 此行为可能会导致外部容器剪切面板。 </p> <p>当设置为<span class="codeph"> fit-vertical </span>时，组件会首先将基板位置移至SocialShare的底部，然后尝试从底部、右侧或左侧推出该面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基板位置移动到顶部，并从顶部、右侧和左侧重复转出尝试。 </p> <p>当设置为<span class="codeph"> fit-later </span>时，组件使用与fit-vertical类似的逻辑，而是将底部向右、向下和向上移动第一尝试方向，然后将底部向左移动，向左、向下和向上移动方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8e843b967237426e9a8b3cd0f27b9820}

可选。

## 默认 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 示例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
