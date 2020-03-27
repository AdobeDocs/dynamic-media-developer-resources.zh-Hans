---
description: Video360查看器的命令参考文档。
seo-description: Video360查看器的命令参考文档。
seo-title: 命令参考- URL
solution: Experience Manager
title: 命令参考- URL
topic: Dynamic media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令参考- URL{#command-reference-url}

Video360查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方 `setParam()`法或/ `setParams()`或两者来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以在某些配置命令前加上类名或相应HTML5查看器SDK组件的实例名。 组件的实例名称是动态的，并取决于传递给 `setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `playback` 说明如下：

```
[Video360Player.|<containerId>_video360Player].playback
```

这意味着此命令的使用方式如下：

* `playback` （短语法）
* `Video360Player.playback` （用组件类名称限定）
* `cont_video360Player.playback` (用组件ID限定，假定 `cont` 它是容器元素的ID)

请参 [阅所有查看器通用的命令参考——所有查看器通用的配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)[和命令参考- URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
