---
title: 使用多個照明地圖
description: 某些應用程式可能需要針對不同材質使用不同的照明地圖。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 使用多個照明地圖{#using-multiple-illumination-maps}

某些應用程式可能需要針對不同材質使用不同的照明地圖。

每個暈映最多可以製作三個照明地圖。 使用下列專案選取彩現操作的照明地圖 `illum=` 和或 `gloss=` 命令。

**預設選取範圍** - If `illum=` 或 `gloss=` 未指定，轉譯器會使用第一個編寫的照明地圖（通常是對應A，亦稱為「平坦」照明地圖）。

**自動選取`gloss=`** - If `illum=` 未指定或設為 `-1`，轉譯器會比較指定的 `gloss=` 值加上與暈映中每個照明地圖相關的光澤值。 它會選擇光澤值最接近指定值的照明地圖 `gloss=`.

**明確選取`illum=`** - If `illum=` 已指定並設為 `0`， `1`，或 `2`，彩現器會使用對應的照明地圖； `gloss=` 會略過選取照明地圖。

如果暈映僅包含一個照明對映，則轉譯器會使用該對映並忽略 `illum=` 和 `gloss=` 命令。
