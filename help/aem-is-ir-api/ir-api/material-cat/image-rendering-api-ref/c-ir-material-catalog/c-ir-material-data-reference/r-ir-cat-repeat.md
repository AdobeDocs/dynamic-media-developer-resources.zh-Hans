---
description: 纹理重复模式。 指定纹理图像如何平铺以填充目标表面。
solution: Experience Manager
title: 重复
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d6946b0-a827-4ee6-963b-84529ad35ee9
TQID: 'https://experienceleague.adobe.com/JK4cutX7dSTk2B2GHfGi1T5yF-382V4o19ZVBewfXGc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 17%

---

# 重复{#repeat}

纹理重复模式。 指定纹理图像如何平铺以填充目标表面。

## 属性 {#section-cef4109cddf54ce095c3293d85bc412d}

枚举。 仅用于可重复纹理。 已忽略所有其他材料。

可重复纹理材料允许使用以下值：

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>0 </p></td> 
  <td class="- topic/stentry stentry"> <p>直接重复。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>1 </p></td> 
  <td class="- topic/stentry stentry"> <p>4向随机拼贴。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>8向随机拼贴。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>菱形拼贴。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>挂上四分之一滴的壁纸。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>三滴壁纸挂着。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>半滴壁纸挂着。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>五滴壁纸挂着。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>倒转墙纸挂着。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>随意挂壁纸。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10 </p></td> 
  <td class="- topic/stentry stentry"> <p>随机放置。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11 </p></td> 
  <td class="- topic/stentry stentry"> <p>随机穿越。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12 </p></td> 
  <td class="- topic/stentry stentry"> <p>半对半对。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13 </p></td> 
  <td class="- topic/stentry stentry"> <p>镜像（书签）。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14 </p></td> 
  <td class="- topic/stentry stentry"> <p>标准随机化器。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15 </p></td> 
  <td class="- topic/stentry stentry"> <p>高频随机化。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16 </p></td> 
  <td class="- topic/stentry stentry"> <p>低频随机化器。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17 </p></td> 
  <td class="- topic/stentry stentry"> <p>水平随机器。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18 </p></td> 
  <td class="- topic/stentry stentry"> <p>垂直随机化。 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19 </p></td> 
  <td class="- topic/stentry stentry"> <p>Edge随机化者。 </p></td> 
 </tr> 
</table>

## 默认 {#section-23fba3bd1f3544c7913d12f2ca148517}

0（直接重复）。

## 另请参阅 {#section-a08887a91db34ed3b183899c69c9f74f}

[重复=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
