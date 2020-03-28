---
description: 'null'
seo-description: 'null'
seo-title: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 拟合横向|拟合垂直</span> </p> </td> 
   <td> <p> 控制下拉面板外观的方向。 </p> <p>当设置为 <span class="codeph"> 适合垂直</span>，组件首先将基板位置移至其按钮的底部，并尝试从基础位置向右或向左滚动面板。 每次尝试时，组件都会检查面板是否被外部容器剪切。 如果所有尝试均失败，则组件会尝试将基板位置移到顶部，并在左右方向重复滚出尝试。 </p> <p>当设置为 <span class="codeph"> 适合横向时</span>，组件使用类似的逻辑，但首先将底座向右移动，尝试向下和向上展开方向。 然后，它把底座向左移动，向下和向上展开。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 为下拉自动隐藏计时器设置延迟时间（以秒为单位），当用户空闲时，该计时器将隐藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-55436ddd78b04f538dbb9a7a8463feae}

可选。

## 默认 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 示例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
