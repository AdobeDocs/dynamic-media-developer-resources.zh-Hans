---
title: 命令引用 — 配置属性
description: 全景查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

全景查看器的配置属性文档。

任何配置命令都可以在URL中设置或使用 `setParam()` 和/或 `setParams()` api方法。 任何配置属性也可以在服务器端配置记录中指定。

某些配置命令可能会带有相应HTML5 SDK组件的类名称或实例名称前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` api方法。 文档将包括此类命令的可选前缀。 例如， `vrrender` 命令记录如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

这意味着此命令按以下方式使用：

* `vrrender` （简短语法）
* `PanoramicView.vrrender` （用组件类名限定）
* `cont_panoramicView.vrrender` （使用组件ID进行限定，假设cont是容器元素的ID）


参见 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

参见 [所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
