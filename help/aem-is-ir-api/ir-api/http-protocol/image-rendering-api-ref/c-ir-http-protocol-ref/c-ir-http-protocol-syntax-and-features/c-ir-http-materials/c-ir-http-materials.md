---
description: 图像渲染将材料应用于晕影中的组或对象。
seo-description: 图像渲染将材料应用于晕影中的组或对象。
seo-title: 材料
solution: Experience Manager
title: 材料
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 材料{#materials}

图像渲染将材料应用于晕影中的组或对象。

材料由一组&#x200B;*属性*&#x200B;组成。 某些材料需要某些属性，而其他属性是可选的，如果存在，则忽略某些属性。 许多属性具有默认值。 并非所有材料都可应用于所有对象（例如，橱柜材料不能应用于沙发）。

服务器会忽略在材料规格段(MSS)中出现但上面或下面特定材料表中未列出的任何属性。

下表列表了基本材料属性。 IR支持控制[高级渲染效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)的其他属性。

除非另有说明，否则所有材料属性都是可选的，具有合适的默认值。

* [纯色](r-ir-solid-colors.md)
* [可重复的纹理](r-ir-repeatable-textures.md)
* [墙边框](r-ir-wall-borders.md)
* [十字](r-ir-decals.md)
* [CAB](r-ir-cabinets.md)
* [窗盖](r-ir-window-coverings.md)
