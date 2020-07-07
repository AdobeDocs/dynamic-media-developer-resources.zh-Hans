---
description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
seo-description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
seo-title: 自定义变量
solution: Experience Manager
title: 自定义变量
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Custom variables{#custom-variables}

请求和晕影的查询部分：修饰符字符串可能包括用户定义的变量。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. 可能由alpha、数字和安全字符的任意组合组成，“$”除外。

** *[!DNL value]* **要设置变量的值（字符串）。

变量的定义与其他服务器命令类似，使用上述语法。 变量必须先定义，才能被引用。 中定义的变 `vignette::Modifier` 量可在URL请求中引用，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必须采用单遍URL编码，才能进行安全HTTP传输。 如果通过HTTP重新传输， *[!DNL value]* 则需要多次编码。 在被替换为嵌套外 *[!DNL value]* 来请求时，会出现这种情况。

变量通过在命令值中嵌入变量名称（由前导和尾随$括起来）来引用。 例如，在命令名称后面的“=”与后面的“&amp;”或请求的结尾之间。 服务器用$$替换每 *[!DNL name]*&#x200B;次出现 *[!DNL string]*。 在命令名称(在命令的 *[!DNL name]*&#x200B;等号之前)和请求的路径部分中出现$$时，不会进行替换。

自定义变量可能不是嵌套的。 任何$$在内 *[!DNL name]*&#x200B;的出现 *[!DNL string]* 都不会被替换。 例如，请求片段解 `$var2=apple&$var1=my$var2$tree&text=$var1$` 析到 `text=my$var2$tree`。

$不是保留字符； 在请求中可能会发生其他情况。 例如， `src=my$texture$file.tif` 是一个有效的命令(假定名为的材料目录条目或纹理文件 [!DNL my$texture$file.tif] 存在)，而 `wid=$number$` 不是，因为需要 `wid=` 一个数字参数。
