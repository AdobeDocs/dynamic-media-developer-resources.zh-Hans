---
description: 資料檔案路徑。 與此影像關聯的非影像資料檔案的相對路徑和名稱。
solution: Experience Manager
title: 輔助路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# 輔助路徑{#auxpath}

資料檔案路徑。 與此影像關聯的非影像資料檔案的相對路徑和名稱。

伺服器會將此值與屬性：：RootPath結合，以建立實際的檔案路徑。 也可以是絕對檔案路徑。

用來指定封包材料的封包樣式檔案，或視窗覆蓋材料的視窗覆蓋樣式檔案。 留空則用於所有其他材料。

## 屬性 {#section-4268350054b7421da0ce0327f0731a52}

文字字串值。 如果已指定，則必須是有效的相對或絕對檔案路徑。 機櫃材料和窗戶覆蓋材料所需。 所有其他材料都必須留空。

## 默认 {#section-287005c2d8e948fa958f69ba7b90b437}

无。

## 另请参阅 {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ， [catalog：：Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)， [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
