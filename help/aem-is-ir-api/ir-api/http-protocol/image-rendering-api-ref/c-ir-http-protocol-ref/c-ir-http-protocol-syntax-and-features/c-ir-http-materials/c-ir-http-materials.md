---
description: “图像渲染”将素材应用于晕影中的组或对象。
solution: Experience Manager
title: 材料
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 材料{#materials}

“图像渲染”将素材应用于晕影中的组或对象。

材料由一组&#x200B;*属性*&#x200B;组成。 某些材料需要某些属性，其他属性是可选的，某些属性会被忽略（如果有）。 许多属性都具有默认值。 并非所有材料都可应用于所有对象（例如，橱柜材料不能应用于沙发）。

服务器会忽略发生在材料规范段(MSS)中但既未列在上面，也未列在以下特定材料表中的任何属性。

下表列表了基本材料属性。 IR支持用于控制[高级渲染效果](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)的其他属性。

除非另有说明，否则所有材料属性都是可选的，具有合适的默认值。

* [纯色](r-ir-solid-colors.md)
* [可重复的纹理](r-ir-repeatable-textures.md)
* [墙边](r-ir-wall-borders.md)
* [十字](r-ir-decals.md)
* [CAB](r-ir-cabinets.md)
* [窗盖](r-ir-window-coverings.md)
