---
title: 标志
description: 套用旗標。 指定其他演算選項。
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

套用旗標。 指定其他演算選項。

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>標幟值。 </p></td> 
 </tr> 
</table>

目前僅用於機櫃材料。

`flags=0` （預設）呈現具有實體門的上方機櫃。

`flags=1` 呈現有玻璃門的上層機櫃（如果暈映是由玻璃門所創作）。

## 屬性 {#section-a2b00d7bb15e449ea85178acb92d8285}

材質屬性。 若非機櫃材料或目標機櫃物件不允許玻璃門，則忽略此項。

## 默认 {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` 無玻璃門。
