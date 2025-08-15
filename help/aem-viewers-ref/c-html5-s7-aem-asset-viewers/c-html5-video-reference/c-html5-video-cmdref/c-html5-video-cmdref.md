---
title: 命令引用 — 配置属性
description: 视频查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

视频查看器的配置属性文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方法`setParam()`和/或`setParams()`来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以使用相应查看器SDK组件的类名或实例名为某些配置命令添加前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`playback`记录如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这表示以下列方式使用此命令

* `playback` （短语法）
* `VideoPlayer.playback` （用组件类名限定）
* `cont_videoPlayer.playback` （用组件ID限定，假设`cont`是容器元素的ID）

查看所有查看者通用的[命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

查看所有查看者通用的[命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
