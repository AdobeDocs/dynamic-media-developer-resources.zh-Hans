---
title: 自定义变量
description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
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

`[!DNL name]`  — 变量名称。 可以由字母、数字和安全字符的任意组合组成，但不包括 `$`.

`[!DNL value]`  — 要将变量设置为的值（字符串）。

变量的定义与其他服务器命令类似，使用上述语法。 必须先定义变量，才能引用它们。 在 `vignette::Modifier` 可以在URL请求中引用，反之则可以。

>[!NOTE]
>
>`[!DNL value]` 必须采用单次URL编码，才能进行安全HTTP传输。 如果 `[!DNL value]` 会通过HTTP重新传输。 这种情况是 `[!DNL value]` 替换为嵌套的外来请求。

变量通过嵌入变量名称来引用（由前导和尾随引用） `$`)的任意位置。 例如，在 `=`  命令名和后续 `&` 或请求结束。 服务器会用 `$ [!DNL name]$` with `[!DNL string]`. 在 `$ [!DNL name]$` 在命令名称（命令的等号之前）和请求的路径部分中。

自定义变量可能无法嵌套。 发生的任何 `$ [!DNL name]$` within `[!DNL string]` 未替换。 例如，请求片段 `$var2=apple&$var1=my$var2$tree&text=$var1$` 解析为 `text=my$var2$tree`.

`$` 不是保留字符；请求中可能会出现其他情况。 例如， `src=my$texture$file.tif` 是有效的命令(假定物料目录条目或纹理文件名为 `[!DNL my$texture$file.tif]` 存在)，而 `wid=$number$` 不是，因为 `wid=` 需要一个数值参数。
