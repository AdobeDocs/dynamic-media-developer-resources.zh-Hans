---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉面板外观的方向。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基础面板位置移动到其按钮的底部，并尝试从基础位置向右或向左转出面板。 在每次尝试时，组件都会检查面板是否被外部容器裁剪。 如果所有尝试都失败，则组件会尝试将基础面板位置移至顶部，并在右侧和左侧重复转出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但先将基面向右移动，然后尝试向下和向上转出方向。 然后，它向左移动基座，尝试向下和向上转出方向。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 设置下拉自动隐藏计时器的延迟（以秒为单位），该计时器会在用户空闲时隐藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-55436ddd78b04f538dbb9a7a8463feae}

可选.

## 默认 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 示例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
