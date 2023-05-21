---
title: 命令參考 — 組態屬性
description: 互動式影像檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

互動式影像檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定或使用 `setParam()`，或 `setParams()`、或兩者。 任何設定屬性也可在伺服器端設定記錄中指定。

某些設定命令可能會加上對應Viewer SDK元件的類別名稱或執行個體名稱當作前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 檔案包含這類命令的選用首碼。 例如， `zoomstep` 命令記錄如下：

`[ZoomView.|<containerId>_zoomView].fmt`

這表示您可以使用此命令作為：

* `fmt` （簡短語法）
* `ZoomView.fmt` （以元件類別名稱限定）
* `cont_zoomView.fmt` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
