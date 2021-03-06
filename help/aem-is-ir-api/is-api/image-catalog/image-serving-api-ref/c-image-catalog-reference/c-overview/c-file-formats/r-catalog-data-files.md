---
description: 目录数据文件可以具有任何名称和文件后缀（.ini除外）。 使用支持制表符分隔的文本数据文件（如Microsoft Excel和Access）的应用程序，可以轻松维护这些配置文件。
solution: Experience Manager
title: 目录数据文件
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 目录数据文件{#catalog-data-files}

目录数据文件可以具有任何名称和文件后缀（.ini除外）。 使用支持制表符分隔的文本数据文件（如Microsoft Excel和Access）的应用程序，可以轻松维护这些配置文件。

目录数据文件本质上是一个二维表，由标头记录组成，用于标识数据列和任意数量的数据记录（行）。 标题和数据记录中的字段用单个`<TAB>`字符分隔。 记录由单个`<CR>`（ASCII代码`0xD`）、单个`<LF>`（ASCII代码`0xA`）或`<CR><LF>`对分隔。

标题记录必须包含每个数据字段的确切名称。 标题行中不允许使用空字段。 数据字段名称不区分大小写。 所有字段名称必须唯一。

空格字符不能用作字段分隔符。 标题记录中不允许有空格。 在数据记录中，数据字段开头或结尾的任何空格都被视为该数据字段的一部分。

在数据记录中，两个相邻的`<TAB>`字符表示一个空字段。 空字段可能会从目录属性或服务器默认值继承默认值。

数据字段可以选择用双引号括起来。 除非数据值为文本类型，且用双引号括住，否则它们不得包含`<CR>`、`<LF>`或`<TAB>`字符。 数据字段不得进行HTTP编码。

同一字段中的多个数据值之间用逗号分隔，除非另有说明。

名称以“。”开头的列 将被忽略。 这允许在图像目录中存储数据，而图像服务对此不感兴趣。 标题名称未知的列将被忽略，并且日志文件中会写入警告。

字段名称可以由ASCII字母、数字以及“ — ”和“_”的任意组合组成。

一个或多个列可用作索引键。 如果同一密钥在同一数据文件中发生多次，则采用后一个实例。
