---
title: 命令引用 — 配置属性
description: 交互式视频查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

交互式视频查看器的配置属性文档。

任何配置命令都可以在URL中设置，或者使用`setParam()`、`setParams()`或API方法同时设置。 任何配置属性也可以在服务器端配置记录中指定。

某些配置命令可能会带有相应Viewer SDK组件的类名称或实例名称前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`playback`命令记录如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

这意味着可以将以下命令用作：

* `playback` （短语法）
* `VideoPlayer.playback` （用组件类名限定）
* `cont_videoPlayer.playback` （用组件ID限定，假设`cont`是容器元素的ID）

另请参阅[所有查看者通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
