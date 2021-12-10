---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`计数`*][, *`淡淡`*][, *`autoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 启用 <span class="codeph"> iconeft</span> 当图像处于重置状态时，显示在图像顶部，并且显示了可用于与图像交互的操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定 <span class="codeph"> iconeft</span> 出现并重新显示。 值 <span class="codeph"> -1</span> 指示图标始终无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡淡</span></span> </p> </td> 
   <td colname="col2"> <p>指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>设置 <span class="codeph"> iconeft</span> 在自动隐藏之前保持完全可见。 即，淡入动画完成后但在淡出动画开始之前的时间。 设置 <span class="codeph"> 0</span> 禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-b6e5e52698d4492f9d6350e7e312bb1b}

可选。

## 默认 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## 示例 {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
