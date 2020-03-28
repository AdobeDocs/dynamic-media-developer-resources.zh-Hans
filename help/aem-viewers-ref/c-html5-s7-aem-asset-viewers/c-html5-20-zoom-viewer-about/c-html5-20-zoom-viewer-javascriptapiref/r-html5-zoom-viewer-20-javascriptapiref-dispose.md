---
description: Zoom Viewer的JavaScript API参考。
seo-description: Zoom Viewer的JavaScript API参考。
seo-title: dispose
solution: Experience Manager
title: dispose
topic: Dynamic media
uuid: 22e6fafa-42e9-4675-a494-66a87a62b7f6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# dispose{#dispose}

Zoom Viewer的JavaScript API参考。

`dispose()`

通过释放查看器逻辑使用的所有资源并删除运行时查看器创建的所有内部对象和组件来处理此查看器实例。

网页代码还应删除查看器实例变量，以便从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器SDK组件上注册事件监听器，或存储了对此类组件的外部引用，则此类监听器必须由网页代码显式地取消注册，且此类外部组件引用必须在调用之前被删除 `dispose()`。

调用后，不再访问Viewer API `dispose()` 。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

