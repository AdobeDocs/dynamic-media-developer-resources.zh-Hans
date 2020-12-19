---
description: 此示例使用图像服务为对象着色，并在一组晕影中应用包含自定义文本的贴体。
seo-description: 此示例使用图像服务为对象着色，并在一组晕影中应用包含自定义文本的贴体。
seo-title: 示例
solution: Experience Manager
title: 示例
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# 示例{#examples}

此示例使用图像服务为对象着色，并在一组晕影中应用包含自定义文本的贴体。

IR变量用于标识暗角、徽标图像和自定义文本。

材料目录`myCat`的暗角图中名为&#x200B;*template*&#x200B;的记录中的`vignette::Modifier`字段包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

将使用的所有晕影列在材料目录`myCat`的晕影图中。

客户端现在可以发出以下请求来检索默认图像（它使用在模板开头定义的变量）:

[!DNL `https://server/myCat/template`]

以下请求指定要呈现的特定内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像服务`text=`命令的详细信息，请参阅图像服务文档。
