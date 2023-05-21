---
description: eCatalog檢視器的設定屬性檔案。
solution: Experience Manager
title: 命令參考 — 組態屬性
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

eCatalog檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定或使用 `setParam()`，或 `setParams()`、或兩者。 您也可以指定伺服器端組態記錄中指定的任何組態屬性。

對於某些組態命令，您可以使用對應Viewer SDK元件的類別名稱或執行個體名稱來加上前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 檔案包含這類命令的選用首碼。 例如， `zoomstep` 命令記錄如下：

`[PageView.|<containerId>_pageView].zoomstep`

這表示您可以使用此命令作為：

* `zoomstep` （簡短語法）
* `PageView.zoomstep` （以元件類別名稱限定）
* `cont_pageView.zoomstep` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
