---
title: 材料
description: “图像渲染”将材质应用于晕影中的组或对象。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# 材料{#materials}

“图像渲染”将材质应用于晕影中的组或对象。

材质由一组&#x200B;*属性*&#x200B;组成。 某些材料需要某些属性，而其他属性是可选的，如果存在，则会忽略某些属性。 许多属性都有默认值。 并非所有材料都可应用到所有对象（例如，无法将机柜材料应用到沙发）。

服务器会忽略在“材料规格段”(MSS)内出现但上面或下面特定材料表中未列出的任何属性。

下表列出了基本材料属性。 IR支持用于控制[高级渲染效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)的其他属性。

除非另有说明，否则所有材料属性都是可选的，并具有适当的缺省值。

* [纯色](r-ir-solid-colors.md)
* [可重复纹理](r-ir-repeatable-textures.md)
* [墙边框](r-ir-wall-borders.md)
* [标记](r-ir-decals.md)
* [文件柜](r-ir-cabinets.md)
* [窗饰](r-ir-window-coverings.md)
