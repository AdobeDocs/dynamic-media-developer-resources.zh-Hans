---
title: 命令參考 — 組態屬性
description: 迴轉檢視器的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

迴轉檢視器的設定屬性檔案。

任何設定命令都可以在URL中設定或使用 `setParam()`，或 `setParams()`、或兩者。 任何設定屬性也可以在伺服器端設定記錄中指定。

某些設定命令可能會加上對應Viewer SDK元件的類別名稱或執行個體名稱當作前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 檔案包含這類命令的選用首碼。 例如， `zoomstep` 命令記錄如下：

`[SpinView.|<containerId>_spinView].zoomstep`

這表示您可以依照以下方式使用此命令

* `zoomstep` （簡短語法）
* `SpinView.zoomstep` （以元件類別名稱限定）
* `cont_spinView.zoomstep` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
