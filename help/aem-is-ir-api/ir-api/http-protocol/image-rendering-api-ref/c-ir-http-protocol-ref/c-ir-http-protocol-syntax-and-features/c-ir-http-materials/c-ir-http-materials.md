---
title: 材料
description: 「影像演算」會將材質套用至暈映中的群組或物件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 材料{#materials}

「影像演算」會將材質套用至暈映中的群組或物件。

材料由一組材料組成 *屬性*. 某些屬性是某些材料的必要屬性，其他屬性則是選用屬性，有些屬性如果存在則會被忽略。 許多屬性都有預設值。 並非所有材料都可套用至所有物件（例如，無法將機櫃材料套用至沙發）。

伺服器會略過任何出現在「材料規格段」(MSS)內，但未列於上方或下方特定材料表中的屬性。

下表列出基本材料屬性。 IR支援其他屬性以控制 [進階演算效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

除非另有註明，否則所有材料屬性都是選用的，並具有適當的預設值。

* [純色](r-ir-solid-colors.md)
* [可重複的紋理](r-ir-repeatable-textures.md)
* [牆邊框](r-ir-wall-borders.md)
* [貼花](r-ir-decals.md)
* [檔案櫃](r-ir-cabinets.md)
* [視窗覆蓋](r-ir-window-coverings.md)
