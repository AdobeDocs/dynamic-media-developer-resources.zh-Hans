---
description: 子选择。 允许将不同材料应用到所选对象或组的不同区域，以及移除先前应用的材料。
seo-description: 子选择。 允许将不同材料应用到所选对象或组的不同区域，以及移除先前应用的材料。
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sub{#sub}

子选择。 允许将不同材料应用到所选对象或组的不同区域，以及移除先前应用的材料。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>选择整个墙。 </p> </td> 
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
  <td class="stentry"> <p>选择顶部墙边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>选择中间墙边框区域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>选择底壁边框区域。 </p> </td> 
 </tr> 
</table>

当前仅支持墙对象。 终止前面的MSS并开始新的MSS以将材料应用于指定的子选择。

为上壁或下壁指定的材料将应用于整个壁，除非为另一半壁指定不同的材料。

## 属性 {#section-b202139d6d0847cc8d520a154104ab9d}

选择命令；MSS分隔符。

## 默认 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 另请参阅 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
