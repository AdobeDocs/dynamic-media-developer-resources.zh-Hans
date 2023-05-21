---
description: 影像的檢視轉換
solution: Experience Manager
title: 影像的檢視轉換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 影像的檢視轉換{#view-transform-for-images}

回應時傳回給使用者端的影像 `req=img` 請求是從複合影像衍生而來，考量了下列值： `wid=`， `hei=`， `fit=`， `scl=`， `rgn=`， `attribute::DefaultPix`， `attribute::MaxPix`，以及複合影像的大小。

若 `wid=` 和 `hei=` 已指定，並且 `scl=` 不會，會縮放複合影像，使其完全符合所定義的檢視矩形 `wid=` 和 `hei=`. 如果檢視矩形的外觀比例與複合影像的外觀比例不同，則縮放後的複合影像會使用 `align=` 值（如果已指定），否則會置中。 影像資料未涵蓋的任何空間都會填滿 `bgc=` 若未指定，則使用 `attribute::BkgColor`.

若 `scl=` 指定時，複合影像會以該縮放係數縮放。 若 `wid=` 和/或 `hei=` 也會指定，縮放的影像隨後會被裁切至 `wid=` 和/或 `hei=` 或視需要新增額外空間。 `align=` 指定影像的裁切位置或新增額外空間，並填滿任何額外空間 `bgc=` 或 `attribute::BkgColor`.

如果兩者都不 `wid=`， `hei=` 也不 `scl=` 指定，如果複合影像的寬度或高度超過 `attribute::DefaultPix`，則複合影像會縮放至不超過 `attribute::DefaultPix`. 否則，複合影像會在不縮放的情況下使用。

若要確保傳回檢視影像時不會進一步縮放，請指定 `scl=1`.

若 `rgn=` 指定，則會據此裁切回覆影像，以獲得最終的回覆影像大小。 此大小會與 `attribute::MaxPix` （若已定義），且如果回覆影像在任一尺寸中較大，則會產生錯誤。

若 `fmt=` 指定不含Alpha的資料，回覆影像中的任何透明區域都會填滿 `bgc=` 或 `attribute::BkgColor`.
