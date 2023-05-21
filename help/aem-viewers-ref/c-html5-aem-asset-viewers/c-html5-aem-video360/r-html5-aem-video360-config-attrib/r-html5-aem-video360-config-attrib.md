---
title: 命令參考 — 組態屬性
description: Video360 Viewer的設定屬性檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

Video360 Viewer的設定屬性檔案。

任何設定命令都可以在URL中設定或使用 `setParam()`，或 `setParams()`、或兩者。 任何組態屬性也可在伺服器端組態記錄中指定。

某些設定命令可能會加上對應Viewer SDK元件的類別名稱或執行個體名稱當作前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 檔案包含這類命令的選用首碼。 例如， `playback` 命令記錄如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

這表示您可以在下列專案使用此命令：

* `playback` （簡短語法）
* `VideoPlayer.playback` （以元件類別名稱限定）
* `cont_videoPlayer.playback` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
