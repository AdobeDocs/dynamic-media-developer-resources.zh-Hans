---
description: 錯誤回應影像。 發生錯誤時，「影像伺服」通常會傳回錯誤狀態並顯示文字訊息。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# ErrorImage{#errorimage}

錯誤回應影像。 發生錯誤時，「影像伺服」通常會傳回錯誤狀態並顯示文字訊息。

`attribute::ErrorImage` 允許設定發生錯誤時要傳回的影像、目錄專案或範本。

>[!NOTE]
>
>遺失的影像也可以透過處理 `attribute::DefaultImage`.

您可以設定「影像伺服」範本，將錯誤訊息文字轉譯為回應影像。 下列預先定義的變數可包含在 `$error.title` 範本，以簡短錯誤說明取代，以及 `$error.message`，以更詳細的錯誤說明取代(詳細資訊層級設定為 `attribute::ErrorDetail`)。

如果可以成功處理錯誤影像/範本，則會傳回HTTP狀態200。 如果在此處理期間發生錯誤，則會傳回HTTP錯誤狀態和文字訊息。

## 屬性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文字字串。 如果已指定，則必須是影像目錄中的有效目錄：：Id值或相對(至 `attribute::RootPath`)或影像伺服器可存取之影像檔案的絕對路徑。

## 默认 {#section-2885f289e5714ddca665a6aee401967f}

繼承自 `default::ErrorImage` 若未定義。 如果已定義但為空，則會停用錯誤影像行為，即使 `default::ErrorImage` 已定義，且會傳回HTTP錯誤狀態和文字訊息。

## 示例 {#section-c92090abe1d247529542a8dd4960c2e6}

若要取得回應影像，並將錯誤訊息演算至影像中，我們首先必須在影像目錄中定義範本。 在此情況下，我們在影像目錄中建立一個名為的專案 `onError`，包含下列專案 `catalog::Modifier`：

`size=300,300&bgc=ffffff&text=$error.message$`

範本註冊於 `attribute::ErrorImage`：

`ErrorImage=myCatalog/onError`

在此範例中，文字會使用預設字型、字型顏色和字型大小呈現。

## 另请参阅 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)， [attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)， [attribute：：ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
