---
description: 视频查看器的配置属性文档。
seo-description: 视频查看器的配置属性文档。
seo-title: 命令引用——配置属性
solution: Experience Manager
title: 命令引用——配置属性
topic: Dynamic Media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 命令引用——配置属性{#command-reference-configuration-attributes}

视频查看器的配置属性文档。

您可以在URL中设置任何配置命令。 或者，可以使用API方法`setParam()`或`setParams()`，或两者来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以在某些配置命令前加上类名或相应查看器SDK组件的实例名。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包括此类命令的可选前缀。 例如，`playback`的说明如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这意味着此命令的使用方式如下：

* `playback` （短语法）
* `VideoPlayer.playback` （限定为组件类名称）
* `cont_videoPlayer.playback` (用组件ID限定，假 `cont` 定它是容器元素的ID)

请参阅所有查看器的通用命令参考——配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[

请参阅所有查看器的通用命令参考- URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[
