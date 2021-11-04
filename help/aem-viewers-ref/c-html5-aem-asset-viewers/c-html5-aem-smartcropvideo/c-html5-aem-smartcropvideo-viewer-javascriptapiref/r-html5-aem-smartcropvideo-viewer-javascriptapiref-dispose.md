---
title: 处置
description: 智能裁剪视频查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# 处置{#dispose}

智能裁剪视频查看器的JavaScript API引用。

`dispose()`

通过释放查看器逻辑使用的所有资源并删除查看器在运行时创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，以便从Web浏览器内存中完全删除查看器。

如果网页代码已在查看器SDK组件上直接注册了事件侦听器（查看器使用）或存储了对此类组件的外部引用，则此类侦听器必须由网页代码显式取消注册。 而且，必须在调用之前删除此类外部组件引用 `dispose()`.

在以下情况下不再访问查看器API `dispose()` 调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
