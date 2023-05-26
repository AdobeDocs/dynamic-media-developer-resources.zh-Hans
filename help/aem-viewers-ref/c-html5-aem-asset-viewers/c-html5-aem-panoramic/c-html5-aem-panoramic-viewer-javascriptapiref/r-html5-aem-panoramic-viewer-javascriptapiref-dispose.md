---
title: 处置
description: 全景查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 4e6ad465-36df-49e2-8c9e-722e8aa9063e
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 处置{#dispose}

全景查看器的JavaScript API参考。

`dispose()`

通过释放查看器逻辑使用的所有资源并在运行时删除查看器创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，并从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器使用的Viewer SDK组件上注册了事件侦听器（或已存储对这些组件的外部引用），则此类侦听器必须由网页代码明确取消注册。 而且，必须在调用之前删除此类外部组件引用 `dispose()`.

之后不再访问查看器API `dispose()` 称为。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
