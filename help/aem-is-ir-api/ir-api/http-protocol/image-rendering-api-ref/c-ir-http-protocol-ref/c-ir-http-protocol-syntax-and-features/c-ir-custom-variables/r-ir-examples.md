---
title: 示例
description: 此示例使用“图像提供”对对象进行着色，并在一组晕影中的某个晕影中应用包含自定义文本的贴士。
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

此示例使用“图像提供”对对象进行着色，并在一组晕影中的某个晕影中应用包含自定义文本的贴士。

IR变量用于识别晕影、徽标图像和自定义文本。

的 `vignette::Modifier` 的字段 *模板* 在材料目录的晕影图上 `myCat` 包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

所有使用的晕影都列在材料目录的晕影图中 `myCat`.

客户端现在可以发出以下请求来检索默认图像（使用模板开头定义的变量）：

[!DNL `https://server/myCat/template`]

以下请求指定要渲染的特定内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像提供的详细信息，请参阅图像提供文档 `text=` 命令。
