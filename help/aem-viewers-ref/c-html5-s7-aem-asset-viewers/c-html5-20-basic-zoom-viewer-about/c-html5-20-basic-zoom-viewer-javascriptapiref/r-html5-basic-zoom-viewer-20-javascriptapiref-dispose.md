---
title: 处置
description: 基本缩放查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 49c353f7-deab-43a7-84dd-21fda7864574
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 处置{#dispose}

基本缩放查看器的JavaScript API引用。

`dispose()`

通过释放查看器逻辑使用的所有资源并删除查看器在运行时创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，以便从Web浏览器内存中完全删除查看器。

如果网页代码已在查看器使用的查看器SDK组件上直接注册了事件侦听器 — 或存储了对此类组件的外部引用 — 则此类侦听器必须由网页代码显式取消注册。 而且，必须在调用之前删除此类外部组件引用 `dispose()`.

在以下情况下不再访问查看器API `dispose()` 调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
