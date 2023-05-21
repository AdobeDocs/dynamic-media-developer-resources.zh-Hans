---
title: 类型
description: 材料曲面型別。 指定材料的曲面型別。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 333b8954-e256-4ba1-8055-c4d625470673
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 17%

---

# 类型{#type}

材料曲面型別。 指定材料的曲面型別。

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>未知，伺服器使用預設值 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>其他 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>天然木材 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>拋光金屬 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>拉絲金屬 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>過時的金屬 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>油漆 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>琺瑯/漆器 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>桌布 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>塑膠 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>實體曲面 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>層壓板 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>乙烯基材料 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>陶瓷 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>天然石頭 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>玻璃 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>映象 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>光纖 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>透明織物 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>地毯 </p></td> 
 </tr> 
</table>

搭配使用 `gloss=` 和 `rough=` 控制反射和光澤效果行為。 不同的材質會產生不同的效果，即使 `gloss=` 和 `rough=` 相同。

## 屬性 {#section-2345b2508273426295ce8ac46182ea64}

材質屬性。 如果暈映不包含3D反射資料，或在暈映中停用光澤效果，則忽略。

## 默认 {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` 如果材料是以型錄專案為基礎。 否則 `type=0`. 若未指定，或 `type=0`時，伺服器會根據目標物件和其他材質屬性，選取合適的預設值。

## 另请参阅 {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ， [粗加工=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
