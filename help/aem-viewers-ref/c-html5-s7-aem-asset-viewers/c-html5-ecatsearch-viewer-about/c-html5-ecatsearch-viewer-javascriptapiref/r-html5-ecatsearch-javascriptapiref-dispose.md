---
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
title: 处置
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 处置{#dispose}

eCatalog查看器的JavaScript API参考。

[!DNL `dispose()`]

通过释放查看器逻辑使用的所有资源并在运行时删除查看器创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，并从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器使用的Viewer SDK组件上注册了事件侦听器，或已存储对这些组件的外部引用，则必须由网页代码显式取消注册此类侦听器，并且必须在调用之前删除此类外部组件引用 [!DNL `dispose()`].

之后不再访问查看器API [!DNL `dispose()`] 称为。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
