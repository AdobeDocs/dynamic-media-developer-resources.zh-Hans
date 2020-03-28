---
description: “图像渲染”将素材应用于晕影中的组或对象。
seo-description: “图像渲染”将素材应用于晕影中的组或对象。
seo-title: 材料
solution: Experience Manager
title: 材料
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# 材料{#materials}

“图像渲染”将素材应用于晕影中的组或对象。

材料由一组属性组 *成*。 某些材料需要某些属性，其他属性是可选的，某些属性如果存在则会被忽略。 许多属性都有默认值。 并非所有材料都可应用于所有对象（例如，橱柜材料不能应用于沙发）。

服务器忽略在材料规范段(MSS)中出现但上面或下面特定材料表中未列出的任何属性。

下表列表了基本材料属性。 IR支持用于控制高级渲染效 [果的其他属性](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)。

除非另有说明，否则所有材料属性都是可选的，并具有合适的默认值。

* [纯色](r-ir-solid-colors.md)
* [可重复的纹理](r-ir-repeatable-textures.md)
* [墙边框](r-ir-wall-borders.md)
* [Decals](r-ir-decals.md)
* [CAB](r-ir-cabinets.md)
* [窗盖](r-ir-window-coverings.md)
