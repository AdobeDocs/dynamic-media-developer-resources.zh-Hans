---
title: 方向
description: 方向
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# 方向{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|左|右</span> </p> </td> 
   <td colname="col2"> <p>指定页面在主视图和缩略图中的显示方式。 它还指定用户与查看器用户界面的交互方式，以便在目录框架之间更改。 </p> <p>当使用<span class="codeph"> left </span>时，它将为初始页面设置右对齐方式，为最后一页设置左对齐方式。 它会按照从左到右的渲染顺序拼接单个页面子图像。 它还将主视图设置为使用从右至左幻灯片动画来推进目录（如果<span class="codeph"> PageView.frametransition </span>设置为幻灯片）。 最后，缩略图设置为从左至右的填充顺序。 </p> <p>同样，当使用<span class="codeph">右</span>时，它将为初始页面设置左对齐方式，为最后一页设置右对齐方式。 它会按照从右到左的渲染顺序拼接单个页面子图像。 它还将主视图设置为使用从左至右幻灯片动画来推进目录（如果<span class="codeph"> PageView.frametransition </span>设置为幻灯片）。 最后，它会反转缩略图顺序，以便按从右至左、从上至下的方向填充缩略图视图。 </p> <p>当设置了<span class="codeph">自动</span>时，当区域设置设置为<span class="codeph"> ja时，查看器应用<span class="codeph">右</span>模式；否则，查看器使用<span class="codeph">左</span>模式。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a66ce10d6c0b449883f654e7e0657e2c}

可选.

## 默认 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 示例 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
