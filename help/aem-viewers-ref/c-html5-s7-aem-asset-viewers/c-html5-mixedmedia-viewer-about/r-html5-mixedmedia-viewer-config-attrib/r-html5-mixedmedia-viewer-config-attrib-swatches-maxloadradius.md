---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
uuid: eb4a6fca-da18-4291-b7fb-e402156c85a0
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定组件预载行为。 设置为<span class="codeph"> -1</span>时，在初始化组件或更改资产时，会同时加载所有色板。 </p> <p>设置为<span class="codeph"> 0</span>时，仅加载可见色板。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 定义预加载可见区域周围的不可见行/列数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
