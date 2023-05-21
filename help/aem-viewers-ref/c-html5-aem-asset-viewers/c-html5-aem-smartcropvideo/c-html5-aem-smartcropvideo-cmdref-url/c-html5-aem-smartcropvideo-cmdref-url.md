---
title: 命令參考 — URL
description: 智慧型裁切視訊檢視器的命令參考檔案。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# 命令參考 — URL{#command-reference-url}

智慧型裁切視訊檢視器的命令參考檔案。

您可以在URL中設定任何組態命令。 或者，您可以使用API方法 `setParam()`，或 `setParams()`，或兩者來設定任何組態命令。 您也可以在伺服器端組態記錄中指定任何組態屬性。

您可以使用類別名稱或對應的Viewer SDK元件的執行個體名稱為某些設定命令加上前置詞。 元件的例項名稱是動態的，且取決於傳遞至的檢視器容器DOM元素的ID `setContainerId()` api方法。 說明檔案包含這類命令的選用首碼。 例如， `playback` 記錄如下：

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

這表示此指令的使用方式如下：

* `playback` （簡短語法）
* `SmartCropVideoPlayer.playback` （以元件類別名稱限定）
* `cont_smartCropVideoPlayer.playback` (以元件ID限定，假設 `cont` 是容器元素的ID)

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

另請參閱 [所有檢視器通用的命令參考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
