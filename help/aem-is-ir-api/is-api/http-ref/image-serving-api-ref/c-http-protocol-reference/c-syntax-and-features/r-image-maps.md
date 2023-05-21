---
description: IS提供簡化HTML影像地圖使用的機制。 IS中的JAVA和Flash型檢視器也包含對影像地圖的有限支援。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 影像地圖{#image-maps}

IS提供簡化HTML影像地圖使用的機制。 IS中的JAVA和Flash型檢視器也包含對影像地圖的有限支援。

來源影像地圖會透過以下方式提供給IS： `catalog::Map` 或使用 `map=` 命令和已處理的地圖會使用 `req=map` 命令。

影像地圖由一或多個HTMLAREA元素組成，並以&#39;&lt;&#39;和&#39;>&#39;正確分隔。 如果透過catalog：：Map提供，則所有畫素座標值都會假設為使用原始影像解析度，並且相對於（未修改的）來源影像的左上角。 若透過 `map=` 指令，座標值會假設為圖層座標，相對於圖層的左上角(在 `rotate=` 和 `extend=`)。

>[!NOTE]
>
>%座標目前不允許使用，且處理方式可能不正確。

IS會透過將空間轉換（例如縮放和旋轉）套用至地圖座標，然後以適當的z順序（從前到後）組裝處理過的圖層地圖，從每個組成圖層的來源影像地圖產生複合影像地圖。

提供下列指令時，會考慮搭配使用於影像地圖處理 `req=map` (直接在請求中、透過目錄範本或在 `catalog::Modifier` 字串)：

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

所有其他指令都會被有效忽略。

此 `SHAPE` 和 `COORDS` 屬性 `AREA` 在處理期間可能修改 `req=map` 請求，的所有其他屬性 `AREA` 傳遞元素時不會進行修改。 在大多數情況下，這涉及到變更 `SHAPE` 值自 `DEFAULT` 至 `RECT` (這也會新增 `COORDS` 屬性)，或變更 `COORDS` 值。

任何 `AREA` 處理期間變為空白的元素會完全移除。 如果地圖與 `layer=comp` 它位於所有其他地圖之後。 資料會以文字形式傳回一個或多個HTML `AREA` 元素。 空白的回覆字串表示指定的物件沒有影像對應。

處理地圖時不考慮圖層透明度。 完全透明的圖層仍然可以有相關聯的影像地圖。 部分透明圖層的對映將不會裁剪至透明區域。

## 另请参阅 {#see-also}

[對應=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ， [catalog：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)， [HTML4.01規格](https://www.w3.org/TR/html401/)
