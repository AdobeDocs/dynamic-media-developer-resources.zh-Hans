---
description: 路径
solution: Experience Manager
title: 路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---

# 路径{#path}

伺服器會使用中所述的路徑解析規則 [管理來源資料](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) 以尋找資料檔案。

## 屬性 {#section-72d9edc532ad43349afcb4df22e1c692}

文字字串。 影像和SVG記錄需要，範本記錄可能空白。 如果已指定，則必須是有效的相對或絕對影像伺服器檔案路徑。 attribute：：DefaultExt若沒有檔案字尾，則會附加。

## 支援的影像檔案格式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

如需支援的影像檔案格式完整清單，請參閱Image Converter (IC)公用程式的說明。

需要多個不同解析度的影像資料的應用程式，在使用Dynamic Media金字塔TIFF(PTIFF)多解析度格式時表現最佳。 IC公用程式可用來從任何支援的影像格式建立PTIFF影像。

## 默认 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

无。

## 另请参阅 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[積體電路公用程式](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)， [attribute：：RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)， [屬性：：DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0)， [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
