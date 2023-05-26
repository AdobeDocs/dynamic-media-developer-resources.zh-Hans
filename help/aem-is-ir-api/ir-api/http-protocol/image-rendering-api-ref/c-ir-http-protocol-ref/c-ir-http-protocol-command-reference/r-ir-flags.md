---
title: 标志
description: 应用标志。 指定其他渲染选项。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# 标志 {#flags}

应用标志。 指定其他渲染选项。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>标志值。 </p></td> 
 </tr> 
</table>

目前仅用于机箱材料。

`flags=0` （默认）渲染带有实体门的上部文件柜。

`flags=1` 呈现带有玻璃门的上层橱柜（如果晕映是由玻璃门创作的）。

## 属性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材质属性。 如果没有机箱材料，或者目标机箱对象不允许使用玻璃门，则忽略此项。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 因为没有玻璃门。
