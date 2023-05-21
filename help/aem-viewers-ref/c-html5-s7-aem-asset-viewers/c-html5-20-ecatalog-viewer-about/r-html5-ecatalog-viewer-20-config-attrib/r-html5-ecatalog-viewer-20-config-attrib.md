---
title: 命令參考 — 組態屬性
description: eCatalog檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

eCatalog檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定或使用 `setParam()`，或 `setParams()`、或兩者。 您也可以指定伺服器端組態記錄中指定的任何組態屬性。

對於某些組態命令，您可以使用對應Viewer SDK元件的類別名稱或執行個體名稱做為前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 檔案包含這類命令的選用首碼。 例如， `zoomstep` 命令記錄如下：

`[PageView.|<containerId>_pageView].zoomstep`

這表示您可以使用此命令作為

* `zoomstep` （簡短語法）
* `PageView.zoomstep` （以元件類別名稱限定）
* `cont_pageView.zoomstep` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
