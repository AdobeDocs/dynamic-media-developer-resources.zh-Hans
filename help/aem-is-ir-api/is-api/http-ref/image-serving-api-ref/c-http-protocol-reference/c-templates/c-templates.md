---
title: 模板
description: 範本可用來減少複合多個影像圖層或包含rtf格式文字之要求的長度和複雜性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 模板{#templates}

範本可用來減少複合多個影像圖層或包含rtf格式文字之要求的長度和複雜性。

自訂變數可用來進一步簡化範本的使用。 範本通常設定為可輕鬆交換影像或文字，或在執行階段設定其他選項。

範本會儲存為影像目錄中的記錄，範本主體會位於 `catalog::Modifier` 欄位，以及 `catalog::Path` 欄位空白或指定無法動態變更的靜態背景影像。

範本是使用 `template=` 命令或在請求URL的路徑元件中。 對於大多數應用程式，建議使用 `template=` 指定範本的命令。 此 `template=`命令不得出現在 `catalog::PostModifier` 欄位，且只能出現在 `catalog::Modifier` 巢狀IS請求中的欄位(即 `src=is{...}` 建構)。 範本記錄不可在中參照 `src=` 或 `mask=`命令。

任何 `src=` 或 `mask=`內嵌在範本中的命令可能會解析為請求的主目錄或不同的影像目錄。 若否 `rootId` 明確指定，則假設是主目錄。 指定的範本 `template=` 也可能位於主目錄或其他影像目錄中。

強烈建議永遠包含範本中使用之所有變數的預設定義。 如此一來，只要指定範本的影像輸出即可，檢視範本的影像輸出 `attribute::RootId` 和 `catalog::Id`，不需知道範本中使用了哪些變數。

預先定義的路徑替代變數 `$object$` 可用來將url路徑中指定的影像物件套用至任何圖層來源或遮色片( `src=` 或 `mask=`)，即使是在巢狀內嵌請求中亦然。

* [範例A](r-example-a.md)
* [範例B](r-example-b.md)
* [範例C](r-example-c.md)
