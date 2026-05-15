---
title: 命令引用 — URL
description: 视频查看器的命令参考文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
TQID: 'https://experienceleague.adobe.com/3FrrEKajCbwAMLGVn8712NSaVChUbQSFUJCs7T6T3-Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# 命令引用 — URL{#command-reference-url}

视频查看器的命令参考文档。

您可以在URL中设置任何配置命令。 或者，您可以使用API方法`setParam()`和/或`setParams()`来设置任何配置命令。 您还可以在服务器端配置记录中指定任何配置属性。

您可以使用相应查看器SDK组件的类名或实例名为某些配置命令添加前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`playback`记录如下：

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

这表示以下列方式使用此命令

* `playback` （短语法）
* `VideoPlayer.playback` （用组件类名限定）
* `cont_videoPlayer.playback` （用组件ID限定，假设`cont`是容器元素的ID）

另请参阅[所有查看者通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

另请参阅所有查看器通用的[命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
