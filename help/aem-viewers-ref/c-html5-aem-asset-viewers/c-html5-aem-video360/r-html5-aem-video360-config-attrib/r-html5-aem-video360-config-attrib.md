---
title: 命令引用 — 配置属性
description: Video360查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

Video360查看器的配置属性文档。

任何配置命令都可以在URL中设置，也可以使用`setParam()`或`setParams()`（或同时使用两者）API方法进行设置。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令可能带有相应查看器SDK组件的类名或实例名的前缀。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `playback`命令记录如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

这表示您可以在以下位置使用此命令：

* `playback` （短语法）
* `VideoPlayer.playback` （使用组件类名称限定）
* `cont_videoPlayer.playback` (使用组件ID进行鉴别， `cont` 假定是容器元素的ID)

另请参阅[所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
