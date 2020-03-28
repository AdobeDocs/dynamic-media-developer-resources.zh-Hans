---
description: 应用标记。 指定其他渲染选项。
seo-description: 应用标记。 指定其他渲染选项。
seo-title: 标志
solution: Experience Manager
title: 标志
topic: Scene7 Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 标志{#flags}

应用标记。 指定其他渲染选项。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>标志值。 </p></td> 
 </tr> 
</table>

当前仅用于机柜材料。

`flags=0` （默认）将上柜呈现为实心门。

`flags=1` 用玻璃门（如果暗角是用玻璃门创作的）绘制上柜。

## 属性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材料属性。 如果不是橱柜材料，或者目标柜对象不允许玻璃门，则忽略。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 没有玻璃门。
