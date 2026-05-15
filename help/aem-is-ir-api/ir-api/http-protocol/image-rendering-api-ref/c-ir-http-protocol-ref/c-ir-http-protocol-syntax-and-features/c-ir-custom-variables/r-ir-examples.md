---
title: 示例
description: 此示例使用图像服务为对象着色，并在一组晕影之一中应用包含自定义文本的贴花。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 1%

---

# 示例{#examples}

此示例使用图像服务为对象着色，并在一组晕影之一中应用包含自定义文本的贴花。

IR变量用于标识晕影、徽标图像和自定义文本。

材质目录`myCat`的晕影映射中名为&#x200B;*template*&#x200B;的记录中的`vignette::Modifier`字段包含以下内容：

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

材质目录`myCat`的晕影映射中列出了所有使用的晕影。

客户端现在可以发出以下请求以检索默认图像（使用在模板开头定义的变量）：

[!DNL `https://server/myCat/template`]

以下请求指定了某些要呈现的内容：

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

有关图像服务`text=`命令的详细信息，请参阅图像服务文档。
