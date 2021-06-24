---
description: 方向
solution: Experience Manager
title: 方向
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|左|右  </span> </p> </td> 
   <td colname="col2"> <p>指定页面在主视图和缩略图中的显示方式。 它还指定了用户与查看器用户界面交互的方式，以便在目录帧之间进行更改。 </p> <p>使用<span class="codeph">左</span>时，它会为初始页面设置右对齐方式，为最后一页设置左对齐方式。 它会按照从左到右的渲染顺序拼合单个页面子图像。 它还会设置主视图以使用从右到左的幻灯片动画来推进目录（如果<span class="codeph"> PageView.frametransition </span>设置为slide）。 最后，为从左到右的填充顺序设置缩略图。 </p> <p>同样，当使用<span class="codeph">右</span>时，它会为初始页面设置左对齐，为最后一页设置右对齐。 它会按从右到左的呈现顺序拼合单个页面子图像。 它还会将主视图设置为使用从左到右的幻灯片动画来推进目录（如果将<span class="codeph"> PageView.frametransition </span>设置为slide）。 最后，将缩览图顺序反转，以便缩览图视图以从右到左、从上到下的方向填充。 </p> <p>设置<span class="codeph">自动</span>后，当区域设置为<span class="codeph"> ja时，查看器将应用<span class="codeph">右</span>模式；</span>否则，它使用左</span>模式的<span class="codeph">。 </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

可选。

## 默认 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 示例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
