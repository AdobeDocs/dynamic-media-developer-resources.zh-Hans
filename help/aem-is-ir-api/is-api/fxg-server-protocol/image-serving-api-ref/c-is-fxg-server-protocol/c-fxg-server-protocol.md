---
title: FXG伺服器通訊協定
description: 要处理图形，您可以使用参考点（类似于罗经点）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 69%

---

# FXG伺服器通訊協定{#fxg-server-protocol}

要处理图形，您可以使用参考点（类似于罗经点）。

使用参考点，您可以相对于某个特定参考点旋转、缩放或调整图形的大小。參照點為 `northWest`， `north`， `northEast`， `west`， `center`， `east`， `southWest`， `south`、和 `southeast`. 例如，使用中心參照點可將圖形中心旋轉45度。 下圖顯示參考點所在的位置、圖形，以及圖形自其旋轉20° `northWest` 參考點，且圖形會從其旋轉20度 `east` 參考點。

![參考點影像](assets/wp_ref_points.png)

* A.參考點位置
* B.圖形
* C.圖形旋轉20度 `northWest` 參考點
* D.圖形旋轉了20° `east` 參考點

语法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

默认值为 none。`inherit` 值将 `s7:referencePoint` 值从页面顶部或组级别传递到所有子项，但前提是它未设置为 `none`。`none` 设置表示该对象没有参考点，使用 FXG 坐标系。

>[!NOTE]
>
>要使用参考点，并且该对象在处理之后不包含任何置换，请在处理新该对象之后更新它的 x 和 y 值。

当`s7:referencePoint` 的值与组（或路径、线元素或任何没有明确定义宽度和高度的元素）一起使用时，该值将应用于该组的累积定界框。例如，该组中所有对象的定界框左上方的点用作该组的 `northWest` 参考点；右下方的点用作 `southEast` 参考点。
