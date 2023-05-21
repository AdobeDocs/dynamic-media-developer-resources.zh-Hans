---
description: getPhotoshopPath作業傳回的影像位置座標。
solution: Experience Manager
title: 四軸透視
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 19%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath作業傳回的影像位置座標。

语法

## 参数 {#section-59792c446366456d90de7f5875bad1b0}

| 名称 | 类型 | 说明 |
|---|---|---|
| x0 | `xsd:double` | 左上x軸座標。 |
| y0 | `xsd:double` | 左上y軸座標。 |
| x1 | `xsd:double` | 右上x軸座標。 |
| y1 | `xsd:double` | 右上y軸座標。 |
| x2 | `xsd:double` | 右下x軸座標。 |
| y2 | `xsd:double` | 右下y軸座標。 |
| x3 | `xsd:double` | 左下x軸座標。 |
| y3 | `xsd:double` | 左下y軸座標。 |

## 示例 {#section-19ed4409ff3a41c9b52a9c9424612927}

此 `PerspectiveQuad` type會依照以下順序傳回資料：

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

