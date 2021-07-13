---
description: “图像渲染”(Image Rendering)将材料应用于晕影中的组或对象。
solution: Experience Manager
title: 材料
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 材料{#materials}

“图像渲染”(Image Rendering)将材料应用于晕影中的组或对象。

材料由一组&#x200B;*属性*&#x200B;组成。 某些材料需要某些属性，而其他属性是可选的，有些属性则会被忽略（如果存在）。 许多属性都具有默认值。 并非所有材料都可应用于所有物体（例如，不能将柜子材料应用于沙发）。

服务器将忽略任何属性，这些属性出现在材料规范段(MSS)中，但上面或下面特定材料表中均未列出。

下表列出了基本材料属性。 IR支持用于控制[高级渲染效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)的其他属性。

除非另有说明，否则所有材料属性都是可选的，并具有适当的默认值。

* [纯色](r-ir-solid-colors.md)
* [可重复的纹理](r-ir-repeatable-textures.md)
* [墙边界](r-ir-wall-borders.md)
* [十字](r-ir-decals.md)
* [CAB](r-ir-cabinets.md)
* [窗盖](r-ir-window-coverings.md)
