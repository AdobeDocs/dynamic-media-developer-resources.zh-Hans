---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: 初始化
solution: Experience Manager
title: 初始化
topic: Dynamic Media
uuid: 142381e4-aa3c-46dd-a0bd-4e090d0003e4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

eCatalog Viewer的JavaScript API参考。

`init()`

开始eCatalog Viewer的初始化。 到此时，必须创建容器DOM元素，以便查看器代码能够按其ID找到它。

如果容器元素尚不是网页布局的一部分（例如，它可能使用分配给它的`display:none`样式进行隐藏），查看器将暂停其初始化过程，直到网页将容器元素重新引回到布局为止。 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期中只调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```

