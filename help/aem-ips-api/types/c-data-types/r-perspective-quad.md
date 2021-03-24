---
description: getPhotoshopPath操作返回的图像位置坐标。
solution: Experience Manager
title: 透视四
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# PerspectiveQuad{#perspectivequad}

getPhotoshopPath操作返回的图像位置坐标。

语法

## 参数 {#section-59792c446366456d90de7f5875bad1b0}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`x0`*` | `xsd:double` | 左上x轴坐标。 |
| `*`y0`*` | `xsd:double` | 左上Y轴坐标。 |
| `*`x1`*` | `xsd:double` | 右上x轴坐标。 |
| `*`y1`*` | `xsd:double` | 右上y轴坐标。 |
| `*`x2`*` | `xsd:double` | 右下x轴坐标。 |
| `*`y2`*` | `xsd:double` | 右下Y轴坐标。 |
| `*`x3`*` | `xsd:double` | 左下X轴坐标。 |
| `*`y3`*` | `xsd:double` | 左下Y轴坐标。 |

## 示例 {#section-19ed4409ff3a41c9b52a9c9424612927}

`PerspectiveQuad`类型按以下顺序返回数据：

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

