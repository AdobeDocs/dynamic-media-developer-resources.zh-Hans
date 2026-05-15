---
description: 在URL或catalog Modifier命令序列中，层定义序列以layer=命令开头，以另一个layer=命令、effect=命令或URL的结尾结尾。
solution: Experience Manager
title: 指定层
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# 指定层{#specifying-layers}

在URL或catalog：：Modifier命令序列中，图层定义序列以layer=命令开头，以另一个layer=命令、effect=命令或URL结尾结尾。

图层定义序列中的所有命令都与图层相关联。

`layer=`命令指定了层号，该层号必须是大于或等于0的整数。 图层定义序列中具有相同图层编号的所有命令都应用于同一图层。 如果同一命令多次出现，则最后一个实例将占上风。
