---
title: 管理頁面標籤
description: 管理頁面標籤
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 管理頁面標籤{#managing-page-labels}

檢視器使用者介面中顯示頁面標籤的位置有兩處：縮圖模式和目錄下拉式清單。

可以定義三種型別的標籤：

* 作者使用SYMBOL本地化機制定義的標籤。
* 作者在Dynamic Media Classic內後端定義的標籤。
* 檢視器自動產生的標籤。

符號型標籤的定義方式 `MediaSet.LABEL_XX[_YY]` 和 `MediaSet.LABEL_DELIM` SYMBOL （如所述） [使用者介面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). 您可以為整個ecatalog跨頁定義此類標籤，在這種情況下，您應使用簡短的SYMBOL語法( `MediaSet.LABEL_XX`)。 或者，使用完整SYMBOL語法( `MediaSet.LABEL_XX_YY`)。

當您為ecatalog跨頁中的兩個頁面定義標籤時，檢視器會使用將這些標籤串連到一個字串中 `MediaSet.LABEL_DELIM` 符號。 SYMBOL型標籤優先於在後端定義的標籤，或由檢視器自動產生的標籤。

Dynamic Media Classic中定義的標籤會儲存在個別頁面影像的UserData記錄中。 與SYMBOL標籤相同。 也就是說，如果eCatalog跨頁中的兩個頁面都定義了標籤，則會使用 `MediaSet.LABEL_DELIM` SYMBOL為橫向模式。 Dynamic Media Classic標籤優先於自動產生的標籤，但會被SYMBOL型標籤所覆寫。

自動產生的標籤是指派給eCatalog中所有頁面的序號。 如果指定的跨頁定義了SYMBOL型標籤或定義了Dynamic Media Classic標籤，則會忽略自動產生的標籤。

在目錄中，可以使用以下方式停用自動產生標籤的顯示 `showdefault` 引數。
