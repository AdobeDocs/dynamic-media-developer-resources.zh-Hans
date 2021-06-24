---
description: 交互式视频查看器的命令参考文档。
solution: Experience Manager
title: 命令引用 — URL
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

交互式视频查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您也可以使用API方法`setParam()`或`setParams()`，或两者都来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以为某些配置命令添加前缀，其中包含类名称或相应查看器SDK组件的实例名称。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `playback`记录如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这表示此命令的使用方式如下：

* `playback` （短语法）
* `VideoPlayer.playback` （使用组件类名称限定）
* `cont_videoPlayer.playback` (使用组件ID进行鉴别，假 `cont` 定是容器元素的ID)

另请参阅[所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另请参阅所有查看器通用的[命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
