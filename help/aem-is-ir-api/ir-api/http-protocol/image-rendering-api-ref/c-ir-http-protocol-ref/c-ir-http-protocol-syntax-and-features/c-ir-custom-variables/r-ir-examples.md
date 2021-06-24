---
description: 此示例使用“图像提供”对对象进行着色，并在一组晕影中的某个晕影中应用包含自定义文本的贴士。
solution: Experience Manager
title: 示例
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# 示例{#examples}

此示例使用“图像提供”对对象进行着色，并在一组晕影中的某个晕影中应用包含自定义文本的贴士。

IR变量用于识别晕影、徽标图像和自定义文本。

物料目录`myCat`晕影图中名为&#x200B;*template*&#x200B;的记录中的`vignette::Modifier`字段包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

将使用的所有晕影都列在材料目录`myCat`的晕影图中。

客户端现在可以发出以下请求来检索默认图像（它使用模板开头定义的变量）：

[!DNL `https://server/myCat/template`]

以下请求指定要渲染的特定内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像服务`text=`命令的详细信息，请参阅图像服务文档。
