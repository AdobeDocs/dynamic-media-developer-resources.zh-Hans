---
title: 命令巨集
description: 指令巨集為指令集提供命名的捷徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 命令巨集{#command-macros}

指令巨集為指令集提供命名的捷徑。

`$ *[!DNL name]*$`

** *[!DNL name]* **巨集名稱

巨集是在個別的巨集定義檔案中定義的，這些檔案可附加至材料目錄或預設目錄。

*[!DNL name]* 不區分大小寫，並且可以包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任何組合。 字符.

在「？」之後的任何請求位置或內的任何位置叫用巨集。 `vignette::Modifier` 欄位。 巨集只能代表一或多個「影像演算」指令，而且必須使用&#39;&amp;&#39;分隔符號與其他指令分隔。

在剖析期間，巨集叫用在其替代字串的早期被取代。 巨集中的命令會覆寫請求中的相同命令（如果這些命令發生在請求中的巨集呼叫之前）。 此工作流程與不同 `vignette::Modifier`，其中請求字串中的命令會覆寫以下專案中的命令： `vignette::Modifier` 字串，無論請求中的位置為何。

命令巨集不能有引數值，但自訂變數可用來將要求中的值傳遞至巨集。

巨集不可巢狀化。

**示例**

如果要將相同的命令或屬性套用到不同的演算影象，巨集就很有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以定義通用屬性的巨集：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

巨集的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

因為 `qlt=` 與第三個要求不同，在叫用巨集後，軟體會覆寫值(指定 `qlt=` *早於* `$render$`無效)。

**另请参阅**

`catalog::MacroFile`， `catalog::Modifier`，巨集定義參考

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
