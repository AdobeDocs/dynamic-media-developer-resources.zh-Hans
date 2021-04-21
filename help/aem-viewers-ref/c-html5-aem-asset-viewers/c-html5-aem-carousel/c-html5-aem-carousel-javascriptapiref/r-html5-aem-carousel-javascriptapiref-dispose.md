---
description: Carousel Viewer的JavaScript API参考。
solution: Experience Manager
title: 处置
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# dispose{#dispose}

Carousel Viewer的JavaScript API参考。

`dispose()`

通过释放查看器逻辑使用的所有资源并删除查看器在运行时创建的所有内部对象和组件，来显示此查看器实例。

网页代码还应删除查看器实例变量，并从Web浏览器内存中完全删除查看器。

如果网页代码已在查看器SDK组件上直接注册了事件侦听器，或存储了对此类组件的外部引用，则此类侦听器必须由网页代码显式地取消注册，并且必须在调用`dispose()`之前删除此类外部组件引用。

在调用`dispose()`后，不再访问查看器API。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
