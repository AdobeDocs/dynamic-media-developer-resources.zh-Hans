---
description: 材料目录优惠了几个功能。
solution: Experience Manager
title: 材料目录*
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---


# 材料目录*{#material-catalogs}

材料目录优惠了几个功能。

* 允许对材料进行持久定义，包括所有材料属性。

   在材料目录中定义的材料可以使用简单的ID而不是一组材料属性进行参照。
* 为某些请求属性（如JPEG质量或默认回复图像大小）提供默认值。
* 管理晕影、ICC用户档案和请求模板。

即使未定义任何特定材料目录，材料目录的所有功能也可通过默认目录([!DNL default.ini])使用。

虽然可以使用材料属性在请求中显式指定渲染材料，但在很多情况下，最好使用材料目录从网站中隐藏材料的详细信息。 src=命令接受目录引用，而不是显式文件路径。 目录条目由` [ *[!DNL catId]*/] *[!DNL itemId]*`组成，其中` *[!DNL catId]*`标识物质目录，` *[!DNL itemId]*`标识目录中的记录。 如果未指定` *[!DNL catId]*`，则使用会话目录（请参阅下文）。

如果(a)` *[!DNL catId]*`与材料目录的`attribute::RootId`值匹配，并且(b)` *[!DNL recId]*`与同一目录中的目录：:Id值匹配，则目录记录将成功匹配。 如果匹配成功，则将材料（包括`src=`）的属性设置为目录记录中的数据。 如果除src=外，MSS还包含此材料的其他属性，则它们会覆盖目录记录中的值。

如果` *[!DNL recId]*`无法与目录条目匹配，则从目录中将` *[!DNL catId]*`替换为`attribute::RootPath`，然后假定生成的路径为简单文件路径。 其他默认属性(例如`attribute::Resolution`)也可以从材料目录中继承。

晕影和ICC用户档案可以在类似于材料本身的材料目录中逐项列出，并指定属性。 此外，晕影图还提供模板的容器。

**另请参阅**

材料目录参考，[ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
