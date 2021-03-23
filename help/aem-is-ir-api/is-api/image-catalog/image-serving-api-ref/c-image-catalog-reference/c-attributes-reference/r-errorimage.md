---
description: 错误响应图像。 图像服务通常在出错时返回带有文本消息的错误状态。
seo-description: 错误响应图像。 图像服务通常在出错时返回带有文本消息的错误状态。
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 1%

---


# ErrorImage{#errorimage}

错误响应图像。 图像服务通常在出错时返回带有文本消息的错误状态。

`attribute::ErrorImage` 允许配置图像、目录条目或模板，以便在出错时返回。

>[!NOTE]
>
>还可以使用`attribute::DefaultImage`处理缺少的图像。

可以配置图像服务模板，该模板可能会将错误消息文本渲染到响应图像中。 `$error.title`模板中可包含以下预定义变量，用短错误描述代替； `$error.message`，用更详细的错误描述代替（详细级别配置为`attribute::ErrorDetail`）。

如果错误图像/模板可以成功处理，则返回HTTP状态200。 如果在此处理过程中发生错误，则返回HTTP错误状态和文本消息。

## 属性 {#section-f460c6c2dd1f46b29f9a79b093575f45}

文本字符串。 如果指定，则必须是图像目录中的有效目录：:Id值，或者是图像服务器可访问的图像文件的相对路径(`attribute::RootPath`)或绝对路径。

## 默认 {#section-2885f289e5714ddca665a6aee401967f}

如果未定义，则从`default::ErrorImage`继承。 如果已定义但为空，则即使已定义`default::ErrorImage` ，错误图像行为也会被禁用，并返回HTTP错误状态和文本消息。

## 示例 {#section-c92090abe1d247529542a8dd4960c2e6}

要获取带有渲染到图像中的错误消息的响应图像，必须首先在图像目录中定义模板。 在这种情况下，我们将在名为`onError`的图像目录中创建一个条目，其中包含`catalog::Modifier`中的以下内容：

`size=300,300&bgc=ffffff&text=$error.message$`

模板已注册`attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

在此示例中，将使用默认字体、字体颜色和字体大小呈现文本。

## 另请参阅 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute:::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
