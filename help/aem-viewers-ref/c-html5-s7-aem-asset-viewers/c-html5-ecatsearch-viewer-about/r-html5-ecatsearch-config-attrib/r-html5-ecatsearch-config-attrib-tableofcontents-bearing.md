---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic Media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉面板外观的方向。 </p> <p>当设置为<span class="codeph"> fit-vertical</span>时，组件首先将基板位置移至其按钮的底部，并尝试从基本位置向右或向左滚出面板。 每次尝试时，组件都会检查面板是否被外部容器剪辑。 如果所有尝试都失败，则组件会尝试将基板位置移至顶部，并在左右方向重复滚出尝试。 </p> <p>当设置为<span class="codeph"> fit-lateral</span>时，组件使用类似的逻辑，但首先将基础向右移动，尝试向下和向上滚出方向。 然后，它把基座向左移动，上下翻开方向。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 设置下拉自动隐藏计时器的延迟（以秒为单位），该计时器在用户空闲时隐藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-55436ddd78b04f538dbb9a7a8463feae}

可选。

## 默认 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 示例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
