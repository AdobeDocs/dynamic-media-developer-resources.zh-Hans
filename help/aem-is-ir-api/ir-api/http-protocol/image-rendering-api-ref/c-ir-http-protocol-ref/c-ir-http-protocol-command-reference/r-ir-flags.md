---
description: 应用标志。 指定其他渲染选项。
seo-description: 应用标志。 指定其他渲染选项。
seo-title: 标志
solution: Experience Manager
title: 标志
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# 标志{#flags}

应用标志。 指定其他渲染选项。

`flags= *`瓦尔`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 瓦尔</span> </p> </td> 
  <td class="stentry"> <p>标志值。 </p></td> 
 </tr> 
</table>

当前仅用于机柜材料。

`flags=0` （默认）呈现上柜的实体门。

`flags=1` 用玻璃门渲染上柜（如果暗角是用玻璃门创作的）。

## 属性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材料属性。 如果不是机柜材料，或者目标机柜对象不允许玻璃门，则忽略。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 没有玻璃门。
