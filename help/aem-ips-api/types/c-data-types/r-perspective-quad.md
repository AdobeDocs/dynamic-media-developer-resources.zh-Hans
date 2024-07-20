---
description: getPhotoshopPath操作返回的图像位置坐标。
solution: Experience Manager
title: 透视四边形
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath操作返回的图像位置坐标。

语法

## 参数 {#section-59792c446366456d90de7f5875bad1b0}

| 名称 | 类型 | 说明 |
|---|---|---|
| x0 | `xsd:double` | 左上x轴坐标。 |
| y0 | `xsd:double` | 左上y轴坐标。 |
| x1 | `xsd:double` | 右上x轴坐标。 |
| y1 | `xsd:double` | 右上y轴坐标。 |
| x2 | `xsd:double` | 右下x轴坐标。 |
| y2 | `xsd:double` | 右下y轴坐标。 |
| x3 | `xsd:double` | 左下x轴坐标。 |
| y3 | `xsd:double` | 左下y轴坐标。 |

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
