---
description: 指令巨集為指令集提供命名的捷徑。
solution: Experience Manager
title: 命令巨集
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 命令巨集{#command-macros}

指令巨集為指令集提供命名的捷徑。

巨集是在個別的巨集定義檔案中定義，這些檔案可附加至影像目錄或預設目錄。

巨集可在&#39;？&#39;之後的任何請求中叫用，也可在內的任何位置叫用。 `catalog::Modifier` 欄位。 巨集只能代表一或多個完整的「影像伺服」命令，因此必須以「&amp;」分隔符號括住（修飾元字串的開頭或結尾除外）。

在剖析期間，巨集叫用在其替代字串的早期被取代。 如果巨集中的命令發生在要求中的巨集呼叫之前，這些命令將會覆寫要求中的相同命令。 這與 `catalog::Modifier`，其中請求字串中的命令一律會覆寫 `catalog::Modifier` 字串，無論請求中的位置為何。

可以巢狀化巨集，但有下列限制：只有在剖析巨集定義時已定義巨集時，才能叫用巨集，方法是先出現在相同的巨集定義檔案中，或將此類內嵌巨集的定義放在預設巨集定義檔案中。

如果要將相同的屬性套用至不同的影像，巨集就很有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我們可以為通用屬性定義巨集：

`view wid=240&fmt=pdf&imageRes=300`

巨集的使用方式如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

從 `wid=` 與第三個請求不同，我們只會覆寫值 *晚於* 呼叫巨集(指定 `wid=`*早於* `$view$` 不會產生任何效果)。

+ [名称](r-name.md)
