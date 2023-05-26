---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上|下|左|右|适合 — 垂直|适合 — 横向 </span> </p> </td> 
   <td colname="col2"> <p> 指定按钮容器的幻灯片动画方向。 </p> <p> 当设置为 <span class="codeph"> 向上 </span>， <span class="codeph"> 下 </span>， <span class="codeph"> left </span>，或 <span class="codeph"> 右 </span>时，面板会以指定方向转出，而不会进行额外的边界检查。 此行为可能导致面板被外部容器剪切。 </p> <p>当设置为 <span class="codeph"> 垂直适合 </span>，组件首先将基础面板位置移到SocialShare的底部，然后尝试从此类基础位置从底部、右侧或左侧转出面板。 在每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并重复从顶部、右侧和左侧转出的尝试。 </p> <p>当设置为 <span class="codeph"> 拟合横向 </span>，组件使用与“适合 — 垂直”类似的逻辑，但组件会将基底移动到右侧，首先尝试右、下和上转出方向，然后将基底移动到左侧，再尝试左、下和上转出方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8e843b967237426e9a8b3cd0f27b9820}

可选.

## 默认 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 示例 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
