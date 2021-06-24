---
description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
solution: Experience Manager
title: 自定义变量
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 自定义变量{#custom-variables}

请求和晕影：：修饰符字符串的查询部分可能包含用户定义的变量。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **变量名称。 可以由字母、数字和安全字符的任意组合组成，不包括“$”。

** *[!DNL value]* **要将变量设置为的值（字符串）。

变量的定义与其他服务器命令类似，使用上述语法。 必须先定义变量，才能引用它们。 在`vignette::Modifier`中定义的变量可以在URL请求中引用，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必须采用单次URL编码，才能进行安全HTTP传输。如果通过HTTP重新传输&#x200B;*[!DNL value]*，则需要进行双重编码。 在将&#x200B;*[!DNL value]*&#x200B;替换为嵌套的外来请求时，即会出现这种情况。

变量通过在命令值中的任意位置嵌入变量名称（由前导和尾随$括起来）来引用。 例如，在命令名称后面的“=”和后续的“&amp;”或请求的结尾之间。 服务器将每次出现$ *[!DNL name]*$的情况替换为&#x200B;*[!DNL string]*。 在命令名称（命令的等号之前）和请求的路径部分中，出现$ *[!DNL name]*$的任何情况都不会发生替换。

自定义变量可能无法嵌套。 在&#x200B;*[!DNL string]*&#x200B;中出现$ *[!DNL name]*$的任何值都不会被替换。 例如，请求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析为`text=my$var2$tree`。

$不是保留字符；请求中可能会出现其他情况。 例如，`src=my$texture$file.tif`是有效的命令（假定存在名为[!DNL my$texture$file.tif]的材料目录条目或纹理文件），而`wid=$number$`则不是，因为`wid=`需要数字参数。
