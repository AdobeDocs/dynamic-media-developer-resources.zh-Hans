---
description: 如果req=img，则合成画布的大小完全由图层0的大小决定。
solution: Experience Manager
title: 合成画布
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# 合成画布{#the-compositing-canvas}

如果req=img，则合成画布的大小完全由图层0的大小决定。

如果未显式指定图层0的`size=`，则使用图层转换计算合成画布的大小（请参阅下文）。

如果`req=tmb`，则合成画布的大小由为图层0指定的`size=`确定；如果未指定大小，则合成画布大小将设置为视图矩形（请参阅下文）。
