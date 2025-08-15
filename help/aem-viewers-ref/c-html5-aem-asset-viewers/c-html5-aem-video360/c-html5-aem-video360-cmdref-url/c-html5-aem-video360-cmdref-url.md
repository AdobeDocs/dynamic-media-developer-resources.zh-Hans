---
title: 命令引用 — URL
description: Video360 Viewer的命令参考文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

Video360 Viewer的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方法`setParam()`和/或`setParams()`来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以使用对应于HTML5 Viewer SDK组件的类名或实例名为某些配置命令添加前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`playback`记录如下：

```
[Video360Player.|<containerId>_video360Player].playback
```

这意味着此命令按以下方式使用：

* `playback` （短语法）
* `Video360Player.playback` （用组件类名限定）
* `cont_video360Player.playback` （用组件ID限定，假设`cont`是容器元素的ID）

查看所有查看者通用的[命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和所有查看者通用的[命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
