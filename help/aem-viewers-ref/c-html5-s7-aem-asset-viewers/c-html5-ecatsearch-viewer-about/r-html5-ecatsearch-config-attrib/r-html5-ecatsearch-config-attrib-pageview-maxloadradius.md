---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，组件会在处于空闲状态时预加载所有目录帧。 </p> <p> 当设置为<span class="codeph"> 0</span>时，组件仅加载可见的帧、上一帧和下一帧。 </p> <p>设置<span class="codeph"><span class="varname"> preloadnbr</span></span>以定义在空闲状态下预加载当前显示帧周围的多少不可见帧。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选.

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
