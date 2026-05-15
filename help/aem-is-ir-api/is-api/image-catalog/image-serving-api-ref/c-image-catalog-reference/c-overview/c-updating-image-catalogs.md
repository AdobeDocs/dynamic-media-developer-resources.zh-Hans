---
description: 服务器连续监视目录文件夹，并在检测到主目录属性文件已更改时自动重新加载图像目录，包括关联的目录数据文件。
solution: Experience Manager
title: 更新图像目录
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
TQID: 'https://experienceleague.adobe.com/vnAa-SrnEWsyYW3PuGQT-CjlhGBB9nkQ20hZSKCUuUw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# 更新图像目录{#updating-image-catalogs}

服务器连续监视目录文件夹，并在检测到主目录属性文件已更改时自动重新加载图像目录，包括关联的目录数据文件。

要更新服务器上的图像目录，请先替换需要更改的所有目录数据文件，然后替换（或“触控”以更新文件日期）目录属性文件以触发目录重新加载。

## 增量更新 {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

加载和处理大型图像目录可能会给服务器带来大量负载，并且可能对实时服务操作产生负面影响。 为了最大程度地降低此影响，建议实施增量目录更新机制，其原理如下：

包含所有图像的主目录文件在低流量时段每夜加载。 如果需要在白天添加或更改图像目录中的记录，则会创建另一个只包含新记录或更改的记录的图像数据文件。 此文件已注册为`attribute::CatalogFile`中的次映像数据文件。 服务器检测目录属性文件已更改，然后检查哪些目录数据文件已更改。 如果尚未接触主图像数据文件，则服务器仅加载或重新加载增量数据文件。 由于此文件通常比主目录文件小得多，因此，与重新加载主目录相比，对服务器的影响要小得多。

增量更新可以显着减少高流量期间对服务器的影响。 建议在低流量时段定期将增量目录数据文件合并到主目录数据文件中，以保持最佳服务器性能。
