---
description: 错误响应图像。 当发生错误时，图像服务通常会返回错误状态并显示一条文本消息。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# ErrorImage{#errorimage}

错误响应图像。 当发生错误时，图像服务通常会返回错误状态并显示一条文本消息。

`attribute::ErrorImage` 允许配置在出错时要返回的图像、目录条目或模板。

>[!NOTE]
>
>缺失的图像也可通过 `attribute::DefaultImage`.

可以配置图像提供模板，以将错误消息文本呈现到响应图像中。 以下预定义变量可包含在 `$error.title` 模板（用简短的错误描述替换）和 `$error.message`，以更详细的错误描述替换(详细程度配置为 `attribute::ErrorDetail`)。

如果错误图像/模板可以成功处理，则返回HTTP状态200。 如果在此处理期间发生错误，则会返回HTTP错误状态和文本消息。

## 属性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文本字符串。 如果已指定，则必须是图像目录中的有效目录：:Id值或相对 `attribute::RootPath`)或图像服务器可访问的图像文件的绝对路径。

## 默认 {#section-2885f289e5714ddca665a6aee401967f}

继承自 `default::ErrorImage` 如果未定义。 如果定义为空，则错误图像行为会被禁用，即使 `default::ErrorImage` 定义，并返回HTTP错误状态和文本消息。

## 示例 {#section-c92090abe1d247529542a8dd4960c2e6}

要获取响应图像，并将错误消息渲染到图像中，必须首先在图像目录中定义模板。 在本例中，我们会在图像目录中创建一个名为 `onError`，在中包含以下内容 `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

模板已在中注册 `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

在本例中，使用默认字体、字体颜色和字体大小呈现文本。

## 另请参阅 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [目录：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [属性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
