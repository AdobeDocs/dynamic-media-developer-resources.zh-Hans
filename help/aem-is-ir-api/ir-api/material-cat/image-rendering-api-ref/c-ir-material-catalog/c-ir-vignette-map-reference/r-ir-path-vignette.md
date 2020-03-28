---
description: 暗角文件路径。 暗角文件的相对路径和名称。
seo-description: 暗角文件路径。 暗角文件的相对路径和名称。
seo-title: 路径
solution: Experience Manager
title: 路径
topic: Scene7 Image Serving - Image Rendering API
uuid: 470cee37-9840-402a-bde5-ace8988996d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 路径{#path}

暗角文件路径。 暗角文件的相对路径和名称。

服务器将此值与此值结合， `attribute::RootPath` 以构建实际的晕影文件路径。 也可以是绝对路径。

## 属性 {#section-b3b295feac084b56bd8a153c04987153}

文本字符串。 可选。如果指定，则它必须是有效的相对或绝对文件路径。 如果为空， `vignette::Modifier` 则必须包含该 `vignette=` 命令。

## 默认 {#section-a1d2133856084eb79a5be8230a4b38fd}

无。

## 另请参阅 {#section-177131dad5804964bfb8957c1f6e5191}

[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
