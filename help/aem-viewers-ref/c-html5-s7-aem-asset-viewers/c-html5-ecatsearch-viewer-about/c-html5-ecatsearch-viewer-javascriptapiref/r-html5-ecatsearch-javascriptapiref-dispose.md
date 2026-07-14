---
title: 处置
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
TQID: 'https://experienceleague.adobe.com/sV3h7e6C2e6lcs24hLgqASaNgMc8wAkcZ9jPvZ-Gz54'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# 处置{#dispose}

eCatalog查看器的JavaScript API参考。

[!DNL `dispose()`]

通过释放查看器逻辑使用的所有资源并在运行时删除查看器创建的所有内部对象和组件来处置此查看器实例。

网页代码还应删除查看器实例变量，并从Web浏览器内存中完全删除查看器。

如果网页代码已直接在查看器使用的SDK组件上注册了事件侦听器（或已存储对这些组件的外部引用），则此类侦听器必须由网页代码明确取消注册。 而且，在调用[!DNL `dispose()`]之前，必须删除此类外部组件引用。

调用[!DNL `dispose()`]后，不再访问查看器API。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例： {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
