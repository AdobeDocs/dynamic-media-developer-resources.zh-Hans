---
title: 自定义变量
description: 请求和晕影修饰符字符串的查询部分可能包含用户定义的变量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# 自定义变量{#custom-variables}

请求和晕影：：修饰符字符串的查询部分可能包含用户定义的变量。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]`  — 变量名称。 可由字母、数字和安全字符的任何组合组成，不包括 `$`.

`[!DNL value]`  — 要设置变量的值（字符串）。

使用上述语法定义的变量与其他服务器命令类似。 必须先定义变量，然后才能引用它们。 在中定义的变量 `vignette::Modifier` 可以在URL请求中引用，反之亦然。

>[!NOTE]
>
>`[!DNL value]` 必须为单通道URL编码，以便安全HTTP传输。 在以下情况下，需要双重编码 `[!DNL value]` 通过HTTP重新传输。 以下情况属于这种情况： `[!DNL value]` 替换为一个嵌套的外部请求。

通过嵌入变量名称（由前导和尾随括住）来引用变量 `$`)命令值中的任意位置。 例如，在 `=`  命令名称后面的 `&` 或请求的结尾。 服务器将每次出现的 `$ [!DNL name]$` 替换为 `[!DNL string]`. 在任何情况下均不会发生替换 `$ [!DNL name]$` （在命令的等号之前）和请求的路径部分中。

自定义变量不能嵌套。 任何出现次数 `$ [!DNL name]$` 范围 `[!DNL string]` 不会被替换。 例如，请求片段 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解析到 `text=my$var2$tree`.

`$` 不是保留字符；否则可能会出现在请求中。 例如， `src=my$texture$file.tif` 是有效的命令(假定材料目录条目或纹理文件名为 `[!DNL my$texture$file.tif]` exists)，而 `wid=$number$` 不是，因为 `wid=` 需要数值参数。
