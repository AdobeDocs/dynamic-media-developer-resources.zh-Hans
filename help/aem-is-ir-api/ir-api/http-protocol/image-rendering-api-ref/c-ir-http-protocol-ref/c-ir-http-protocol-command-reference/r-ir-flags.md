---
description: 应用标记。 指定其他渲染选项。
solution: Experience Manager
title: 标志
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# 标志{#flags}

应用标记。 指定其他渲染选项。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>标记值。 </p></td> 
 </tr> 
</table>

目前仅用于机柜材料。

`flags=0` （默认）呈现带实体门的上机柜。

`flags=1` 呈现带玻璃门的上柜（如果晕影是用玻璃门创作的）。

## 属性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材料属性。 如果不是机柜材料，或者目标机柜对象不允许玻璃门，则忽略。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 没有玻璃门。
