---
title: IccProfileGray
description: 灰度默认色彩空间。 指定未使用icc=指定输出色彩空间时用于灰度响应图像的ICC颜色配置文件的名称。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# IccProfileGray{#iccprofilegray}

灰度默认色彩空间。 指定未指定输出色彩空间时用于灰度响应图像的ICC色彩配置文件的名称 `icc=`.

## 属性 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

文本字符串。 如果已指定，则必须是有效的 `icc::Name` 此材料目录或默认目录的ICC配置文件映射中的值，或相对于 `attribute::RootPath`. 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

继承自 `default::IccProfileGray` 如果未定义或为空。

## 另请参阅 {#section-cd43189611f4426aacddcc604eb02a10}

[icc:：名称](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [属性：:IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
