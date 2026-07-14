---
title: 自定义变量
description: 请求和晕影修饰符字符串的查询部分可能包含用户定义的变量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
TQID: 'https://experienceleague.adobe.com/1-o3GqgzwvPYV8UDBuZu5udOiG-p8Tue3Fo-ft8-QhI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 0%

---

# 自定义变量{#custom-variables}

请求和晕影：：修饰符字符串的查询部分可能包含用户定义的变量。

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` — 变量名称。 可由字母、数字和安全字符的任意组合组成，不包括`$`。

`[!DNL value]` — 要设置变量的值（字符串）。

使用上述语法定义的变量与其他服务器命令类似。 必须先定义变量，然后才能引用它们。 在`vignette::Modifier`中定义的变量可以在URL请求中引用，反之亦然。

>[!NOTE]
>
>`[!DNL value]`必须为单通道URL编码，以便安全HTTP传输。 如果通过HTTP重新传输`[!DNL value]`，则需要双重编码。 将`[!DNL value]`替换为嵌套式外部请求时会出现这种情况。

通过在命令值中的任意位置嵌入变量名称（由前导和尾随`$`括起来）来引用变量。 例如，在命令名称后面的`=`与后续`&`或请求结尾之间。 服务器将每个出现的`$ [!DNL name]$`替换为`[!DNL string]`。 在命令名称（在命令的等号之前）和请求的路径部分中`$ [!DNL name]$`的任何匹配项都不会发生替换。

自定义变量不能嵌套。 在`[!DNL string]`内出现的`$ [!DNL name]$`均不会被替换。 例如，请求片段`$var2=apple&$var1=my$var2$tree&text=$var1$`解析为`text=my$var2$tree`。

`$`不是保留字符；它可能在请求中出现。 例如，`src=my$texture$file.tif`是有效的命令（假定存在名为`[!DNL my$texture$file.tif]`的材质目录条目或纹理文件），而`wid=$number$`则否，因为`wid=`需要数值参数。

