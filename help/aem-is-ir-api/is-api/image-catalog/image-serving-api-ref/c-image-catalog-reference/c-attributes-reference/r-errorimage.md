---
description: 错误响应图像。 当发生错误时，图像服务通常会返回错误状态并显示一条文本消息。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# ErrorImage{#errorimage}

错误响应图像。 当发生错误时，图像服务通常会返回错误状态并显示一条文本消息。

`attribute::ErrorImage` 允许配置在出错时要返回的图像、目录条目或模板。

>[!NOTE]
>
>`attribute::DefaultImage`也可以处理缺少的图像。

可以配置图像提供模板，以将错误消息文本呈现到响应图像中。 以下预定义变量可包含在`$error.title`模板中（用短错误描述替换）和`$error.message`（用更详细的错误描述替换）（详细级别配置为`attribute::ErrorDetail`）。

如果错误图像/模板可以成功处理，则返回HTTP状态200。 如果在此处理期间发生错误，则会返回HTTP错误状态和文本消息。

## 属性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文本字符串。 如果已指定，则必须是图像目录中的有效目录：:Id值，或者是图像服务器可访问的图像文件的相对路径(`attribute::RootPath`)或绝对路径。

## 默认 {#section-2885f289e5714ddca665a6aee401967f}

从`default::ErrorImage`继承（如果未定义）。 如果已定义但为空，则即使定义了`default::ErrorImage`并返回HTTP错误状态和文本消息，错误图像行为也会被禁用。

## 示例 {#section-c92090abe1d247529542a8dd4960c2e6}

要获取响应图像，并将错误消息渲染到图像中，必须首先在图像目录中定义模板。 在本例中，我们将在图像目录中创建一个名为`onError`的条目，该条目包含`catalog::Modifier`中的以下内容：

`size=300,300&bgc=ffffff&text=$error.message$`

模板已在`attribute::ErrorImage`中注册：

`ErrorImage=myCatalog/onError`

在本例中，将使用默认字体、字体颜色和字体大小呈现文本。

## 另请参阅 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
