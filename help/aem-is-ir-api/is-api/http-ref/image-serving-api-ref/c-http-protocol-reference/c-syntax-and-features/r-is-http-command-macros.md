---
description: 指令巨集為指令集提供命名的捷徑。 巨集是在個別的巨集定義檔案中定義，這些檔案可附加至影像目錄或預設目錄。
solution: Experience Manager
title: 命令巨集
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# 命令巨集{#command-macros}

指令巨集為指令集提供命名的捷徑。 巨集是在個別的巨集定義檔案中定義，這些檔案可附加至影像目錄或預設目錄。

`$ *`名称`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名稱</span></span> </p> </td> 
  <td class="stentry"> <p>巨集名稱。 </p></td> 
 </tr> 
</table>

`*`名稱`*` 不區分大小寫，而且可能包含ASCII字母、數字、&#39;-&#39;、&#39;_&#39;和&#39;.&#39;的任何組合。 字符.

巨集可在&#39;？&#39;之後的任何請求中叫用，也可在內的任何位置叫用。 `catalog::Modifier` 或 `catalog::PostModifier` 欄位。 巨集只能代表一或多個完整的「影像伺服」命令，而且必須使用&#39;&amp;&#39;分隔符號與其他命令分開。

在剖析期間，巨集叫用在其替代字串的早期被取代。 如果巨集中的命令發生在要求中的巨集呼叫之前，這些命令將會覆寫要求中的相同命令。 這與 `catalog::Modifier`，其中請求字串中的命令一律會覆寫 `catalog::Modifier` 字串，無論請求中的位置為何。

命令巨集不能有引數值，但自訂變數可用來將要求中的值傳遞至巨集。

可以巢狀化巨集，但有下列限制：只有在剖析巨集定義時已定義巨集時，才能叫用巨集，方法是先出現在相同的巨集定義檔案中，或將此類內嵌巨集的定義放在預設巨集定義檔案中。

## 示例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果要將相同的屬性套用至不同的影像，巨集就很有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我們可以為通用屬性定義巨集：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

巨集的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

從 `wid=` 與第三個請求不同，我們只會覆寫值 *晚於* 呼叫巨集(指定 `wid=`*早於* `$view$` 不會產生任何效果)。

## 另请参阅 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog：：MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ， [catalog：：Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)， [巨集定義參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
