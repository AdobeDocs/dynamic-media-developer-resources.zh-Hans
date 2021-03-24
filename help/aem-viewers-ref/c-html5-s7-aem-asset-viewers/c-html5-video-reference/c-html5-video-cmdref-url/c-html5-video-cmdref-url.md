---
description: 视频查看器的命令参考文档。
solution: Experience Manager
title: 命令参考 — URL
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 命令引用 — URL{#command-reference-url}

视频查看器的命令参考文档。

可以在URL中设置任何配置命令。 或者，可以使用API方法`setParam()`或`setParams()`，或两者来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以在某些配置命令前添加类名或相应查看器SDK组件的实例名的前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包括此类命令的可选前缀。 例如，`playback`的说明如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这意味着此命令的使用方式如下：

* `playback` （短语法）
* `VideoPlayer.playback` （限定为组件类名称）
* `cont_videoPlayer.playback` (使用组件ID限定，假 `cont` 定该ID是容器元素的ID)

另请参阅[所有查看器的通用命令参考 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另请参阅所有查看器的通用命令参考 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。[
