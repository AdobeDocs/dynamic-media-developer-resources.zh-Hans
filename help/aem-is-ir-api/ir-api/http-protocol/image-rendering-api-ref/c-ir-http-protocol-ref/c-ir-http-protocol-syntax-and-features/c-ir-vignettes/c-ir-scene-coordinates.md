---
description: 场景坐标空间用于指定可纹理化对象曲面上的大小和距离。
solution: Experience Manager
title: 场景坐标
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# 场景坐标{#scene-coordinates}

场景坐标空间用于指定可纹理化对象曲面上的大小和距离。

由于大多数晕影是描绘物理对象的真实场景，因此大多数晕影是使用英寸作为场景坐标空间的单位创作的。 其它单位，如mm或cm也可以使用。 “图像渲染”不支持单元转换。

以下命令接受场景坐标空间中的值：

* [格劳特=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [大小=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
