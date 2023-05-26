---
title: 命令引用 — URL
description: 交互式视频查看器的命令参考文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

交互式视频查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方法 `setParam()`，或 `setParams()`，或同时使用两者来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以使用相应查看器SDK组件的类名称或实例名称为某些配置命令添加前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` api方法。 文档包含此类命令的可选前缀。 例如， `playback` 记录如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这意味着此命令按以下方式使用

* `playback` （简短语法）
* `VideoPlayer.playback` （用组件类名限定）
* `cont_videoPlayer.playback` (用组件ID限定，假设 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

另请参阅 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
