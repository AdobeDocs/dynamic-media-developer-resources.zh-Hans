---
title: 材料目录
description: 材料目录提供了几个功能。
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

材料目录提供了几个功能。

* 允许持久定义材料，包括所有材料属性。

   可以使用简单ID引用材料目录中定义的材料，而不是使用一组材料属性。
* 提供某些请求属性的默认值，例如JPEG质量或默认回复图像大小。
* 管理晕影、ICC配置文件和请求模板。

即使未定义特定的材料目录，材料目录的所有特征也可通过缺省目录( [!DNL default.ini])。

虽然渲染材料可以在使用材料属性的请求中显式指定，但通常更希望通过使用材料目录从网站中隐藏材料的详细信息。 src=命令接受目录引用而不是显式文件路径。 目录条目包括 ` [ *[!DNL catId]*/] *[!DNL itemId]*`，其中 ` *[!DNL catId]*` 标识材质目录和 ` *[!DNL itemId]*` 标识目录中的记录。 如果 ` *[!DNL catId]*` 未指定，将使用会话目录（请参阅下文）。

如果(a)符合以下条件，则已成功匹配目录记录 ` *[!DNL catId]*` 匹配 `attribute::RootId` 材料目录价值和(b) ` *[!DNL recId]*` 匹配同一目录中的catalog：：Id值。 如果成功匹配，则材料属性(包括 `src=`)设置为目录记录中的数据。 如果MSS在src=之外还包含此材料的其他属性，则会覆盖目录记录中的值。

如果 ` *[!DNL recId]*` 无法与目录条目匹配，则 ` *[!DNL catId]*` 替换为 `attribute::RootPath` 之后，将目录和生成的路径假定为简单文件路径。 其他默认属性(例如， `attribute::Resolution`)也可以从材料目录中继承。

晕影和ICC轮廓可以在与材料本身类似的材料目录中逐项列出，并且给定属性。 此外，晕影映射还为模板提供了容器。

**另请参阅**

材料目录参考， [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)， `attribute::RootId`， `attribute::RootPath`， `attribute::VignettePath`
