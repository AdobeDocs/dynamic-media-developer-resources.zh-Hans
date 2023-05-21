---
description: 影像演算支援根據符合ICC （國際色彩聯盟）規格的色彩空間設定檔進行色彩空間轉換。
solution: Experience Manager
title: 影像演算色彩管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 影像演算色彩管理*{#image-rendering-color-management}

影像演算支援根據符合ICC （國際色彩聯盟）規格的色彩空間設定檔進行色彩空間轉換。

**限制**

目前僅支援CMYK、RGB和灰階色彩空間。

封包樣式檔案(.vnc)和視窗覆蓋樣式檔案( [!DNL .vnw])不是色彩管理，且被假定存在於工作色域中。

**另请参阅**

[國際色彩協會](https://www.color.org/index.xalter) ， [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ， [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ， `attribute::IccProfile*` ， `attribute::IccProfileSrc*`， `attribute::IccRenderIntent` ， `attribute::IccBlackPointCompensation` ， `attribute::IccDither` ，ICC設定檔對應

## 預設色彩空間 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每個影像目錄（和預設目錄）可以定義一組ICC設定檔。 這些設定檔構成此目錄的預設色彩空間 — 灰階、RGB和CMYK資料各有一個輸入和一個輸出設定檔( `attribute::IccProfileRgb`， `attribute::IccProfileGray`， `attribute::IccProfileCmyk`， `attribute::IccProfileSrcRgb`， `attribute::IccProfileSrcGray`、和 `attribute::IccProfileSrcCmyk`)。

系統會根據影像的畫素型別，從目錄預設設定檔中選取特定影像或其他物件的預設色域。

## 輸入色域 {#section-660f661a7e954df4b451e34134195276}

材質影像可內嵌ICC設定檔以定義輸入色域。 如果來源影像中未內嵌任何設定檔， `attribute::IccProfileSrc*` 會使用與來源影像的畫素型別對應的適用影像目錄中的。 如果未在影像目錄中定義此屬性， `attribute::IccProfile*` 已使用。 如果該目錄屬性也未定義，則影像不會以顏色管理，且只會套用天真的轉換。

## 工作色域 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，有效色域是由暈映中內嵌的ICC色彩設定檔所定義。 如果暈映不包含設定檔，預設RGB輸入設定檔( `attribute::IccProfileSrcRgb` （工作階段目錄），用於工作色域。

所有演算作業都會在工作色彩空間中執行。

**重要：** 工作色域的ICC設定檔必須支援輸入和輸出轉換。 如果僅輸出輪廓用作工作色域，IR將無法將材質轉換為它。 如果材質存在於相同的工作色域中，仍可使用這種色彩輪廓。 嘗試在其他色彩空間套用材質會失敗。

## 明確的顏色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

指定的色彩值RGB `color=`， `bgc=`， `catalog::BgColor`、和 `catalog::Color` 被假定存在於目前的工作色域中。

## 材質資料檔案 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材質影像檔案（紋理和貼花影像）可以有RGB、灰階或CMYK畫素型別，並可以嵌入色彩設定檔。 如果沒有內嵌色彩輪廓，預設的輸入色彩空間會與影像相關聯（例如，材料目錄中的色彩輪廓，會與影像的畫素型別相對應）。

從巢狀影像提供或影像演算請求獲得的材質影像通常包含色彩設定檔。 如果不是這種情況，則影像會與畫素型別對應的預設輸入色域相關聯。

如果影像檔案的色域與使用中的色域不同，則會使用精確的色彩轉換來轉換為使用中的色域。 若未內嵌設定檔且未定義預設輸入設定檔，則會使用天真型別轉換。

其他材質資料檔案，例如封包樣式檔案( [!DNL .vnc])或視窗涵蓋範圍檔案( [!DNL .vnw])不要內嵌色彩設定檔，且一律假定在工作色域中。

## 輸出色域 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有演算作業都會在工作色彩空間中進行。 如果要求指定了不同的色彩設定檔 `icc=` 命令中，資料會在編碼並傳回使用者端之前先轉換至該色域。 停用色彩管理時，如有必要，會使用天真的轉換來轉換為灰階或CMYK。

## 內嵌色彩設定檔 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

與演算後的影像相關聯的色彩設定檔可透過指定以下專案嵌入回應影像中 `iccEmbed=` 請求。

若 `icc=` 未指定，則會內嵌工作色域的ICC設定檔。 如果停用色彩管理且未指定任何設定檔，則不會內嵌任何設定檔 `icc=`.

## ICC 配置文件 {#section-afeb76068b5042adb83261638e450140}

伺服器使用的所有色彩設定檔都必須符合ICC規格。 ICC設定檔通常會 [!DNL .icc] 或 [!DNL .icm] 檔案字尾，並與材質資料檔案共存。

雖然輸出設定檔可透過中的檔案路徑/名稱來指定 `icc=` 指令，建議在預設目錄或特定材料目錄的「ICC輪廓對映」中註冊所有輪廓檔案，並使用快捷方式識別碼( `icc::Name`)而非檔案路徑。

工作輪廓必須在材料目錄或預設目錄的「ICC輪廓對映」中註冊。
