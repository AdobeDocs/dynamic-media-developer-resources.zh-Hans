---
description: 影像檔案路徑。
solution: Experience Manager
title: 路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---

# 路径{#path}

影像檔案路徑。

與此目錄記錄相關聯的來源影像檔案的相對或絕對路徑與名稱。 伺服器會使用管理來源資料中所述的路徑解析規則來尋找資料檔案。

## 屬性 {#path-properties}

文字字串。 影像記錄需要，範本記錄可能空白。 如果已指定，則必須是有效的相對或絕對影像伺服器檔案路徑。 attribute：：DefaultExt若沒有檔案字尾，則會附加。

## 支援的影像檔案格式 {#path-supported-image-file-formats}

如需支援檔案格式的完整清單，請參閱Image Converter (IC)公用程式的說明。

需要多個不同解析度的影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時表現最佳。 IC公用程式可用來從任何支援的影像格式建立PTIFF影像。

## 默认 {#path-default}

无。

## 另请参阅 {#path-seealso}

[積體電路公用程式](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ， [attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ， [屬性：：DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ， [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
