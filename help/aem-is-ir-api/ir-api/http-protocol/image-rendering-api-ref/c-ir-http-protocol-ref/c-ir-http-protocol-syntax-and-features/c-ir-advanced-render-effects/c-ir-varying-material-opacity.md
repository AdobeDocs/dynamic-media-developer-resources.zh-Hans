---
description: 对应用于重叠对象以及贴花和窗口覆盖材料的纯色和可重复纹理支持可变不透明度。
seo-description: 对应用于重叠对象以及贴花和窗口覆盖材料的纯色和可重复纹理支持可变不透明度。
seo-title: 改变材料不透明度
solution: Experience Manager
title: 改变材料不透明度
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# 改变材料不透明度{#varying-material-opacity}

对应用于重叠对象以及贴花和窗口覆盖材料的纯色和可重复纹理支持可变不透明度。

只需将RGB图像与Alpha渠道一起使用，即可提供不透明度信息。 此外，可以使用`opacity=`命令（对于RGB和RGBA图像）来改变整体不透明度。

壁边框还支持RGBA图像，主要用于支持模切边框。

定义窗口覆盖的[!DNL vnw]文件可以包括不透明度渠道，该不透明度渠道由渲染器与可重复纹理的alpha和`opacity=`值组合，以提供用于透明和半透明窗口处理的全范围不透明度效果。
