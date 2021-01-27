---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: 处置
solution: Experience Manager
title: 处置
topic: Dynamic Media
uuid: b2073d03-a0a0-4f55-a350-7336ddcf031d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# dispose{#dispose}

eCatalog Viewer的JavaScript API参考。

`dispose()`

通过释放查看器逻辑使用的所有资源并删除运行时查看器创建的所有内部对象和组件，来处置此查看器实例。

网页代码还应删除查看器实例变量，以从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器SDK组件上注册事件监听器，或存储了对此类组件的外部引用，则此类监听器必须由网页代码显式地取消注册，且必须在调用`dispose()`之前删除此类外部组件引用。

调用`dispose()`后，不再访问查看器API。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

