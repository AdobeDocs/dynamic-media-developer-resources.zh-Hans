---
title: 示例
description: 此示例使用图像服务为对象着色，并在一组晕影之一中应用包含自定义文本的贴花。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# 示例{#examples}

此示例使用图像服务为对象着色，并在一组晕影之一中应用包含自定义文本的贴花。

IR变量用于标识晕影、徽标图像和自定义文本。

材质目录`vignette::Modifier`的晕影映射中名为&#x200B;*template*&#x200B;的记录中的`myCat`字段包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

材质目录`myCat`的晕影映射中列出了所有使用的晕影。

客户端现在可以发出以下请求以检索默认图像（使用在模板开头定义的变量）：

[!DNL `https://server/myCat/template`]

以下请求指定了某些要呈现的内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像服务`text=`命令的详细信息，请参阅图像服务文档。
