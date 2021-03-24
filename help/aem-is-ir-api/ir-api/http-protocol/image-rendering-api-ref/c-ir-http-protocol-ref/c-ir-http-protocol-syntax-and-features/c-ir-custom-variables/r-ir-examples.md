---
description: 此示例使用图像服务为对象着色，并在一组晕影中应用包含自定义文本的贴片。
solution: Experience Manager
title: 示例
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 示例{#examples}

此示例使用图像服务为对象着色，并在一组晕影中应用包含自定义文本的贴片。

IR变量用于标识晕影、徽标图像和自定义文本。

材料目录`myCat`的晕影图中名为&#x200B;*template*&#x200B;的记录中的`vignette::Modifier`字段包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

将使用的所有晕影都列在材料目录`myCat`的晕影图中。

客户端现在可以发出以下请求来检索默认图像（它使用在模板开头定义的变量）：

[!DNL `https://server/myCat/template`]

以下请求指定要渲染的特定内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像服务`text=`命令的详细信息，请参阅图像服务文档。
