---
description: 请求和晕影修饰符字符串的查询部分可能包括用户定义的变量。
seo-description: 请求和晕影修饰符字符串的查询部分可能包括用户定义的变量。
seo-title: 自定义变量
solution: Experience Manager
title: 自定义变量
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Custom variables{#custom-variables}

请求和晕影：：修饰符字符串的查询部分可能包括用户定义的变量。

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. 可能由alpha、数字和安全字符的任意组合组成，“$”除外。

** *[!DNL value]* **要设置变量的值（字符串）。

变量的定义与其他服务器命令类似，使用上述语法。 变量必须先定义，然后才能被引用。 中定义的变量 `vignette::Modifier` 可以在URL请求中引用，反之亦然。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>*[!DNL value]* 必须采用单次URL编码，才能进行安全HTTP传输。 如果通过HTTP重新传输， *[!DNL value]* 则需要多次编码。 在嵌套外来请求中 *[!DNL value]* 被替换为这种情况。

变量通过在命令值中的任意位置嵌入变量名称（由前导和尾随$括起）来引用。 例如，在命令名后的&#39;=&#39;与后续的&#39;&amp;&#39;或请求的结尾之间。 服务器将每次出现的$ *[!DNL name]*$替换为 *[!DNL string]*。 在命令名称中（在命令的等号之前）和请求的路径部分中出现$ *[!DNL name]*$，不会发生替换。

自定义变量不能嵌套。 不替换$ *[!DNL name]*$内的 *[!DNL string]* 任何实例。 例如，请求片段解 `$var2=apple&$var1=my$var2$tree&text=$var1$` 析为 `text=my$var2$tree`。

$不是保留字符；在请求中可能会出现其他情况。 例如，是 `src=my$texture$file.tif` 一个有效的命令(假定名为的材料目录条目或纹理文件 [!DNL my$texture$file.tif] 存在)，而 `wid=$number$` 不是，因为需要 `wid=` 一个数字参数。
