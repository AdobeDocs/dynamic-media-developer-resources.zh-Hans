---
title: 处置
description: 适用于混合媒体查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e09f73a9-a961-4188-b092-f7bbcae4946d
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 处置{#dispose}

适用于混合媒体查看器的JavaScript API参考。

`dispose()`

通过释放查看器逻辑使用的所有资源并在运行时删除查看器创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，并从Web浏览器内存中完全删除查看器。

如果网页代码直接在查看器使用的Viewer SDK组件上注册了事件侦听器，或者存储了对这些组件的外部引用，则此类侦听器必须由网页代码明确取消注册。 而且，在调用`dispose()`之前，必须删除此类外部组件引用。

调用`dispose()`后，不再访问查看器API。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
