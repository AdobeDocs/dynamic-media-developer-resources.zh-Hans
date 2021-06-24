---
description: 子选择。 允许将不同材料应用于所选对象或组的不同区域，以及移除先前应用的材料。
solution: Experience Manager
title: sub
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 7%

---

# sub{#sub}

子选择。 允许将不同材料应用于所选对象或组的不同区域，以及移除先前应用的材料。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>选择整个壁。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>选择墙的上半部分。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>选择墙的下半部分。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>选择顶壁边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择中间壁边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>选择底壁边框区域。 </p> </td> 
 </tr> 
</table>

当前仅支持壁对象。 终止前一个MSS，并为要应用于指定子选择的材料启动新的MSS。

为上壁或下壁指定的材料将应用于整个壁，除非为另一半壁指定了不同的材料。

## 属性 {#section-b202139d6d0847cc8d520a154104ab9d}

选择命令；MSS分隔符。

## 默认 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 另请参阅 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
