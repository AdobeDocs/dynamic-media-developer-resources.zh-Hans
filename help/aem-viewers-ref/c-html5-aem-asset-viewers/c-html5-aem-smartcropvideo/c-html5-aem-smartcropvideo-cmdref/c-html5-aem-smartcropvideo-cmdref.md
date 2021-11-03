---
title: 命令引用 — 配置属性
description: 智能裁剪视频查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

智能裁剪视频查看器的配置属性文档。

您可以在URL中设置任何配置命令。 或者，您也可以使用API方法 `setParam()`或 `setParams()`，或同时用于设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以为某些配置命令添加前缀，其中包含类名称或相应查看器SDK组件的实例名称。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `playback` 记录如下：

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

这表示此命令的使用方式如下：

* `playback` （短语法）
* `SmartCropVideoPlayer.playback` （使用组件类名称限定）
* `cont_videoPlayer.playback` (使用组件ID进行鉴别，假定 `cont` 是容器元素的ID)

请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

请参阅 [所有查看器 — URL通用的命令引用](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
