---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: 791c47e9-daab-4500-9cd0-e56ee6fc830e
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# dispose{#dispose}

eCatalog Viewer的JavaScript API参考。

[!DNL `dispose()`]

通过释放查看器逻辑使用的所有资源并删除运行时查看器创建的所有内部对象和组件来处理此查看器实例。

网页代码还应删除查看器实例变量，以便从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器SDK组件上注册事件监听器，或存储了对此类组件的外部引用，则此类监听器必须由网页代码显式地取消注册，且此类外部组件引用必须在调用之前被删除 [!DNL `dispose()`]。

调用后，不再访问Viewer API [!DNL `dispose()`] 。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

