---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 适合 — 横向|适合 — 垂直</span> </p> </td> 
   <td> <p> 控制下拉面板外观的方向。 </p> <p>当设置为 <span class="codeph"> 垂直适合</span>时，组件会先将基础面板位置移动到其按钮的底部，然后尝试从基础位置向右或向左滚动面板。 在每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并在右侧和左侧重复转出尝试。 </p> <p>当设置为 <span class="codeph"> 拟合横向</span>，组件使用类似的逻辑，但会先将基面移动到右侧，然后尝试向下和向上转出方向。 然后，它将底部向左移动，尝试向下和向上转出方向。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 设置下拉自动隐藏计时器的延迟（以秒为单位），当用户空闲时，该计时器会隐藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-55436ddd78b04f538dbb9a7a8463feae}

可选.

## 默认 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 示例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
