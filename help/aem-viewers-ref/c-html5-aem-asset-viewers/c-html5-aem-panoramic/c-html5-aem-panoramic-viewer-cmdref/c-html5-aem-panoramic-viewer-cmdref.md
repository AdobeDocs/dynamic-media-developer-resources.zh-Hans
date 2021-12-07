---
title: 命令引用 — 配置属性
description: 全景查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

全景查看器的配置属性文档。

可以在URL中或使用 `setParam()` 和/或 `setParams()` API方法。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令可能带有相应HTML5 SDK组件的类名或实例名的前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档将包含此类命令的可选前缀。 例如， `vrrender` 命令将记录如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

这表示此命令的使用方式如下：

* `vrrender` （短语法）
* `PanoramicView.vrrender` （使用组件类名称限定）
* `cont_panoramicView.vrrender` （使用组件ID进行鉴别，假定续是容器元素的ID）


请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

请参阅 [所有查看器 — URL通用的命令引用](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
