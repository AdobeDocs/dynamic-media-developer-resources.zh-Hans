---
description: 影像地圖資料。 提供此圖層的影像地圖資料。 覆寫此圖層的目錄地圖中的所有資料。
solution: Experience Manager
title: 地图
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 地图{#map}

影像地圖資料。 提供此圖層的影像地圖資料。 覆寫此圖層的catalog：：Map中的所有資料。

`map=[ *`字串`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>圖層座標中此圖層的影像地圖資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>以來源影像座標表示此圖層的影像地圖資料。 </p></td> 
 </tr> 
</table>

空白字串表示此圖層不應提供影像地圖。 該字串必須正確進行HTTP編碼，以避免剖析問題。

中出現的所有與號(&amp;)字元 *`string`* 必須為http編碼。

當 `mapA=` 和 `catalog::Map` 以來源影像座標指定地圖資料， `map=` 相對於圖層矩形的左上角，假定圖層座標(在 `rotate=` 和 `extend=` （已套用）。

輸出影像地圖一律會裁剪至圖層矩形。 如果 `shape` 屬性被省略或設為 `default`，則整個圖層矩形會作為影像地圖區域使用。

## 屬性 {#section-a18d9ea95c71414a905a68b8839c0843}

圖層屬性。 套用至 `layer=comp`，則指定的地圖資料會圖層式地置於所有其他影像地圖之後。 已忽略，除非 `req=map`. 被效果圖層忽略。 `mapA=` 被忽略，如果 `map=` 也會指定。

## 默认 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 使用時機 `map=` 未指定。

## 示例 {#section-cd7691c94f984222845c86dcb0051ce8}

為簡單文字圖層定義矩形影像地圖：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

一個 `AREA` 具有（通常）預設屬性的元素可用來插入整個圖層矩形的對映區域。

## 另请参阅 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[影像地圖](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)， [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
