---
title: 命令引用 — URL
description: Video360查看器的命令参考文档。
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

Video360查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您也可以使用API方法`setParam()`或`setParams()`，或两者都来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以为某些配置命令添加前缀，其中包含类名称或相应HTML5查看器SDK组件的实例名称。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `playback`记录如下：

```
[Video360Player.|<containerId>_video360Player].playback
```

这表示此命令的使用方式如下：

* `playback` （短语法）
* `Video360Player.playback` （使用组件类名称限定）
* `cont_video360Player.playback` (使用组件ID进行鉴别，假 `cont` 定是容器元素的ID)

请参阅所有查看器的通用命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)和[所有查看器通用的命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)[
