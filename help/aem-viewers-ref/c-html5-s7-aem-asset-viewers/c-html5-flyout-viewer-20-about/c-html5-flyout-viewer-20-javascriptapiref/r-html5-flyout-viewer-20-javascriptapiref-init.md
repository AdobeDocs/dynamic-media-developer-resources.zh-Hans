---
title: init
description: 适用于弹出查看器初始化的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
TQID: 'https://experienceleague.adobe.com/vavSoeUebo8YrntPoPKm3why-Jbzrh4p6v8Eqmgsv1I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# init{#init}

弹出查看器的JavaScript API参考。

`init()`

启动弹出查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以按其ID找到它。

例如，如果容器元素还不是网页布局的一部分，则可以使用分配给它的`display:none`样式将其隐藏，查看器将暂停其初始化过程。 一直到网页将容器元素重新放置到布局时为止。 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期内只应调用一次此方法，随后的调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`对查看器实例的引用。

## 示例： {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
