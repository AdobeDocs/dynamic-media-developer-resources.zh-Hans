---
description: 遮色片檔案路徑。 與此目錄記錄相關聯的遮色片影像檔案的相對或絕對路徑與名稱。
solution: Experience Manager
title: 遮色片路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# 遮色片路徑{#maskpath}

遮色片檔案路徑。 與此目錄記錄相關聯的遮色片影像檔案的相對或絕對路徑與名稱。

允許將個別遮色片附加至影像。

伺服器會使用中所述的路徑解析規則 [管理來源資料](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) 以尋找資料檔案。

## 屬性 {#section-cdc3b7e2811e41008479cd97887c01b7}

文字字串值。 可选. 如果已指定，則必須是有效的相對或絕對影像伺服器檔案路徑。 `attribute::DefaultExt` 如果不存在檔案字尾，則會附加。

如果兩個主要影像( `catalog::Path`)和遮色片影像( `catalog::MaskPath`)定義於目錄記錄中，兩者必須具有相同畫素大小。 遮色片影像必須是8位元灰階。

`mask=` 在要求中覆寫 `catalog::MaskPath`.

`catalog::MaskPath` 覆寫主影像中的Alpha色版( `catalog::Path`)，如果有的話，以及Alpha色版未相關聯的話（即未預先乘法）。 如果影像Alpha是預乘， `catalog::MaskPath` 會忽略，且一律使用Alpha色版。

## 默认 {#section-78533e35bfec469ba087cb68a35bb81b}

无。

## 另请参阅 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ， [屬性：：DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)， [catalog：：Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)， [遮色片=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)， [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
