---
title: sub
description: 子选择。 允许将不同的材料应用到所选对象或组的不同区域，并移除先前应用的材料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 7%

---

# sub{#sub}

子选择。 允许将不同的材料应用到所选对象或组的不同区域，并移除先前应用的材料。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>选取整个壁。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>选择壁的上半部。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>选择壁的下半部。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>选择顶壁边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择中壁边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>选择下壁边框区域。 </p> </td> 
 </tr> 
</table>

当前仅支持墙对象。 终止先前的MSS并为要应用于指定子选区的材料启动新的MSS。

为上壁或下壁指定的材料应用于整个壁，除非为另一半壁指定了不同的材料。

## 属性 {#section-b202139d6d0847cc8d520a154104ab9d}

选择命令；MSS分隔符。

## 默认 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 另请参阅 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
