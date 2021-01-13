---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，组件在空闲状态下预加载所有目录帧。 </p> <p> 当设置为<span class="codeph"> 0</span>时，组件仅加载当前可见的帧、上一帧和下一帧。 </p> <p>设置<span class="codeph"><span class="varname"> preloadnbr</span></span>以定义当前显示的帧周围有多少不可见帧处于空闲状态。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选。

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
