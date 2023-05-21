---
description: 漸進式JPEG掃描。 漸進式JPEG顯示影像的方式，使其一開始會顯示整個模糊/低品質像片。 隨著掃描過程繼續進行，影像的資料下載得越充分，掃描過程就越清晰。 此引數可讓您設定顯示整個影像所需的掃描次數（3、4或5）。
solution: Experience Manager
title: pscan
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# pscan{#pscan}

漸進式JPEG掃描。 漸進式JPEG顯示影像的方式，使其一開始會顯示整個模糊/低品質像片。 隨著掃描過程繼續進行，影像的資料下載得越充分，掃描過程就越清晰。 此引數可讓您設定顯示整個影像所需的掃描次數（3、4或5）。

`pscan=auto|3|4|5`

每次掃描的實際速度取決於使用者系統和接收及解壓縮資料的電腦的傳輸速度。

`Auto` 使用由獨立JPEG庫計算並取決於顏色模型的掃描設定。 的值 `3`， `4`， `5` 對應至將JPEG檔案儲存為pjpeg (漸進式JPEG)時，在Adobe Photoshop中找到的「掃描」設定。

若 `pscan` 未設定，其預設值為 `auto`.

## 屬性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

要求屬性。 無論目前的圖層設定為何，均適用。 如果輸出格式不是漸進式JPEG，則忽略。

## 默认 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 示例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另请参阅 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
