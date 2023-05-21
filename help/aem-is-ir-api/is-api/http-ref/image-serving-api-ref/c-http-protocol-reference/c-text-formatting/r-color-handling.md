---
description: RTF規格允許以&bsol；colortbl指定的RGB色彩值。 每個元件分別提供&bsol；red、&bsol；green和&bsol；blue指令。
solution: Experience Manager
title: 色彩處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 色彩處理{#color-handling}

RTF規格允許指定的RGB色彩值 `\colortbl`. 每個元件都獨立提供， `\red`， `\green`、和 `\blue` 命令。

專屬RTF延伸命令 `\cmykcolortbl` 允許指定CMYK顏色，每個顏色元件都隨附於 `\cyan`， `\magenta`， `\yellow`、和 `\black` 命令。

的顏色元件值 `\colortbl` 介於0到255之間。 下列專案的元件值 `\cmykcolortbl` 介於0到100之間。

RTF延伸命令 `\*\iscolortbl`，支援者 `textPs=`，可讓您指定具有標準「影像伺服」色彩值的色彩表，並支援完整RGB、灰色、CMYK和Alpha。 其語法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一或多個IS色彩值，以「；」分隔

可以在同一個中指定多種型別的色彩表 `text=` 或 `textPs=` rtf字串。 每個色彩表可以有不同的專案數量。 「影像伺服」會嘗試依照以下順序尋找顏色： `\iscolortbl` 早於 `\cmykcolortbl` （僅當文字圖層的畫素型別是CMYK時） `\colortbl`. 對象 `textPs=` 只有在需要時(例如指定RGB顏色但需要CMYK輸出時)，才會在CMYK和RGB之間精確轉換顏色。 如果找不到特定索引值的顏色，則會使用預設顏色（黑色）。

請參閱 [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 以取得IS色彩值的語法說明。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支援 `\*\iscolortbl`. `textPs=` 不支援 `\cmykcolortbl`.

呈現Photofonts時會忽略顏色選取範圍。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允許使用變數控制三種文字色彩，同時當在標準RTF文字編輯器中開啟RTF字串時仍顯示色彩預設值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
