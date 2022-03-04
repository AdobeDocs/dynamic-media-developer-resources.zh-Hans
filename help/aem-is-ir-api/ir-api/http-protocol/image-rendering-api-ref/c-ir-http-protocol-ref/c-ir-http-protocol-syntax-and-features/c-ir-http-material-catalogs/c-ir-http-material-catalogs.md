---
title: 材料目录
description: 材料目录提供多项功能。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 材料目录 {#material-catalogs}

材料目录提供多项功能。

* 允许对材料进行持久定义，包括所有材料属性。

   在材料目录中定义的材料可以使用简单的ID来引用，而不是使用一组材料属性。
* 为某些请求属性(如JPEG质量或默认回复图像大小)提供默认值。
* 管理小图、ICC配置文件和请求模板。

即使未定义任何特定材料目录，材料目录的所有特征也可通过默认目录( [!DNL default.ini])。

虽然可以在使用材料属性的请求中明确指定渲染材料，但通常更需要使用材料目录从网站中隐藏材料的详细信息。 src=命令接受目录引用，而不是显式文件路径。 目录条目由 ` [ *[!DNL catId]*/] *[!DNL itemId]*`，其中 ` *[!DNL catId]*` 识别材料目录， ` *[!DNL itemId]*` 在目录中标识记录。 如果 ` *[!DNL catId]*` 未指定，则使用会话目录（请参阅下文）。

如果(a) ` *[!DNL catId]*` 匹配 `attribute::RootId` (b)物料目录之价值 ` *[!DNL recId]*` 与同一目录中的catalog::Id值匹配。 如果匹配成功，则材料(包括 `src=`)会设置为目录记录中的数据。 如果除src=之外，MSS还包含此材料的其他属性，则它们将覆盖目录记录中的值。

如果 ` *[!DNL recId]*` 无法与目录条目匹配，则 ` *[!DNL catId]*` 替换为 `attribute::RootPath` 之后，将假定从目录中删除并生成路径为简单的文件路径。 其他默认属性(例如， `attribute::Resolution`)也可从材料目录继承。

可在与材料本身和给定属性类似的材料目录中逐项列出小角和ICC配置文件。 此外，晕影图还为模板提供了容器。

**另请参阅**

材料目录参考、 [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
