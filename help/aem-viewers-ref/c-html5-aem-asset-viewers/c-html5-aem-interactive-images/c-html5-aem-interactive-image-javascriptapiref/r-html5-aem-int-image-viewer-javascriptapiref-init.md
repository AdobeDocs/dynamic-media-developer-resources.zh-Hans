---
title: init
description: 交互式图像查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 675031ab-21bb-49a5-abbc-eca8d2619e49
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

交互式图像查看器的JavaScript API参考。

`init()`

启动交互式图像查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以按其ID找到它。

如果容器元素还不是网页布局的一部分 — 例如，它可能会使用以下项目隐藏 `display:none` 为其指定的样式 — 查看器暂停其初始化过程。 一直到网页将容器元素带回布局为止。 执行此操作后，查看器加载会自动恢复。

在查看器生命周期内仅调用此方法一次；后续调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
