---
title: 命令引用 — 配置属性
description: 智能裁剪视频查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# 命令引用 — 配置属性{#command-reference-configuration-attributes}

智能裁剪视频查看器的配置属性文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方法 `setParam()`，或 `setParams()`，或同时使用两者来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以使用相应查看器SDK组件的类名称或实例名称为某些配置命令添加前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` api方法。 文档包含此类命令的可选前缀。 例如， `playback` 记录如下：

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

这意味着此命令按以下方式使用：

* `playback` （简短语法）
* `SmartCropVideoPlayer.playback` （用组件类名限定）
* `cont_videoPlayer.playback` (用组件ID限定，假设 `cont` 是容器元素的ID)

参见 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

参见 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
