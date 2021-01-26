---
description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
seo-description: 请求和晕影修饰符字符串的查询部分可以包括用户定义的变量。
seo-title: 自定义变量
solution: Experience Manager
title: 自定义变量
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# 自定义变量{#custom-variables}

请求和晕影的查询部分：修饰符字符串可能包括用户定义的变量。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **变量名称。 可能由alpha、数字和安全字符的任意组合组成，“$”除外。

** *[!DNL value]* **要设置变量的值（字符串）。

变量的定义与其他服务器命令类似，使用上述语法。 变量必须先定义，才能被引用。 在`vignette::Modifier`中定义的变量可以在URL请求中引用，反之亦然。

>[!NOTE]
>
>*[!DNL value]* 必须采用单遍URL编码，才能进行安全HTTP传输。如果通过HTTP重新传输&#x200B;*[!DNL value]*，则需要多次编码。 在将&#x200B;*[!DNL value]*&#x200B;替换为嵌套外来请求时，会出现这种情况。

变量通过在命令值中嵌入变量名称（由前导和尾随$括起来）来引用。 例如，在命令名称后面的“=”与后面的“&amp;”或请求的结尾之间。 服务器将每次出现$ *[!DNL name]*$替换为&#x200B;*[!DNL string]*。 在命令名称（在命令的等号之前）和请求的路径部分中出现$ *[!DNL name]*$的任何替换都不会发生。

自定义变量可能不是嵌套的。 未替换&#x200B;*[!DNL string]*&#x200B;中出现的$ *[!DNL name]*$的任何情况。 例如，请求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析为`text=my$var2$tree`。

$不是保留字符；在请求中可能会发生其他情况。 例如，`src=my$texture$file.tif`是一个有效命令（假定存在名为[!DNL my$texture$file.tif]的材料目录条目或纹理文件），而`wid=$number$`则不是，因为`wid=`需要一个数字参数。
