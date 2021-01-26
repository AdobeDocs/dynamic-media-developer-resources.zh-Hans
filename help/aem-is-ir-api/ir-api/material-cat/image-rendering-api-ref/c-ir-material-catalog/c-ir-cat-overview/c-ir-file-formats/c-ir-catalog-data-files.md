---
description: 目录数据文件可以具有任何名称和文件后缀（.ini除外）。
seo-description: 目录数据文件可以具有任何名称和文件后缀（.ini除外）。
seo-title: 目录数据文件
solution: Experience Manager
title: 目录数据文件
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# 目录数据文件{#catalog-data-files}

目录数据文件可以具有任何名称和文件后缀（.ini除外）。

使用支持制表符分隔的文本文件（如Microsoft Excel和Access）的应用程序，可轻松维护目录数据文件。

从本质上讲，目录数据文件是一个二维表，它包含一个标头记录，它标识数据列和任意数量的数据记录（行）。 标题和数据记录中的字段以单个`<TAB>`字符分隔。 记录由单个`<CR>`（ASCII代码0xD）、单个`<LF>`（ASCII代码0xA）或`<CR><LF>`对分隔。

标题记录必须包含每个数据字段的确切名称。 标题行中不允许使用空字段。 数据字段名称不区分大小写。 所有字段名称必须唯一。

除`<TAB>`字段分隔符外，标题和数据记录中不允许有空格。

在数据记录中，相邻的两个`<TAB>`字符表示一个空字段。 空字段将从目录属性或服务器默认值继承默认值。

数据字段不得包含`<CR>`、`<LF>`或`<TAB>`字符，除非数据值是文本类型，且用单引号或多次引号括起来。 数据字段不能进行HTTP编码。

除非另有说明，否则同一字段中的多个数据值以逗号(“,”)分隔。

名称开始为“.”的列 被忽略；这允许将数据存储在图像渲染不感兴趣的材料目录中。 标题名称未知的列将被忽略，并且日志文件中会写入警告。

字段名称可能由ASCII字母、数字以及“-”和“_”的任意组合组成。

一个或多个列可用作索引键。 如果同一数据文件中多次出现同一密钥，则以后的实例为准。
