---
title: 命令引用 — URL
description: 视频查看器的命令参考文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

视频查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您也可以使用API方法 `setParam()`或 `setParams()`，或同时用于设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以为某些配置命令添加前缀，其中包含类名称或相应查看器SDK组件的实例名称。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `playback` 记录如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这表示此命令的使用方式如下

* `playback` （短语法）
* `VideoPlayer.playback` （使用组件类名称限定）
* `cont_videoPlayer.playback` (使用组件ID进行鉴别，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

另请参阅 [所有查看器 — URL通用的命令引用](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
