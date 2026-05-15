---
description: 设置修剪边距。 设置PDF文件中设置的修剪边距。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
TQID: 'https://experienceleague.adobe.com/xrj1Qk8XDpN0r45H5uB2rkq6cq2xP8sn5LobTtKtxG4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 0%

---

# trimMargin{#trimmargin}

设置修剪边距。 设置PDF文件中设置的修剪边距。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`分

默认情况下，`trimMargin`设置为由`viewWidth`和`viewHeight`定义的文档的完整大小。 如果未指定，*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值将默认为&#x200B;*[!DNL top]*&#x200B;值。
