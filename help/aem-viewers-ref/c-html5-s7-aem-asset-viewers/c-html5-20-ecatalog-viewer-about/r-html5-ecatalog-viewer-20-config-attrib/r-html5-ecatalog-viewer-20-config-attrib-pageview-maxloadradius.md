---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预载行为。 </p> <p>当设置为 <span class="codeph"> -1</span> 组件在空闲状态下预加载所有目录帧。 </p> <p> 当设置为 <span class="codeph"> 0</span> 组件仅加载当前可见的帧、上一帧和下一帧。 </p> <p>设置 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定义在空闲状态下预载当前显示帧周围的多少不可见帧。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选.

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
