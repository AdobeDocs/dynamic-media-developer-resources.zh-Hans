---
description: 文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。
seo-description: 文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。
seo-title: 文本字符串本地化
solution: Experience Manager
title: 文本字符串本地化
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 文本字符串本地化{#text-string-localization}

文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。

服务器将与指定的区域设置相匹配的表示返回到客户端 `locale=`，从而避免客户端本地化，并且允许应用程序只通过发送具有IS文本请求的适当值来切换 `locale=` 区域设置。

## 范围 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文本字符串本地化应用于以下目录字段中包含本地化令 ` ^loc= *`牌locId`*^` 的所有字符串元素：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目录字段</b> </th> 
   <th class="entry"> <b>字段中的字符串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素(由分隔符',' ';' ':'和／或字段的开始/结尾的任意组合分隔)。 </p> <p> 可本 <span class="codeph"> 地化字 </span> 段开头的0xrrggbb颜色值从本地化中排除并传递而不进行修改。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>除coords=和shape=属性的值外，任何单引号或多次引号的 <span class="codeph"> 属性值 </span> 都 <span class="codeph"> 是 </span> 例外。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:目标 </span> </p> </td> 
   <td> <p>任何目标的 <span class="codeph"> 值。*.label </span> 和 <span class="codeph"> 目标。*.userdata属 </span> 性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字符串语法 {#section-d12320edf300409f8e17565b143acafc}

图像目录 *`string`* 中启用本地化的元素由一个或多个本地化字符串组成，每个字符串前面都有本地化令牌。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> string <span class="varname"> Element </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken localized </span> String <span class="varname"></span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 本 <span class="varname"> 地化令牌 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>本地化令牌后的本地化 <span class="varname"> 字符串 </span> 的内部区 <span class="varname"> 域设置ID </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 本地化 <span class="varname"> 的字符串 </span></span> </p> </td> 
  <td class="stentry"> <p>本地化的字符串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span></span> </p> </td> 
  <td class="stentry"> <p>用于未知区域设置的字符串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必须为ASCII，且不能包括“^”。

无论是否使用HTTP编码，子字符串中的任何位置都可能出现“^”。 服务器将整个模式与 *`localizationToken`*`^loc=locId^` 单独的子字符串匹配。

*`stringElements`* 不包括至少一项 *`localizationToken`* 的本地化。

## 翻译图 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定义服务器用来确定哪个规则 *`localizedStrings`* 返回到客户端的规则。 它由一列表输入(与指定的 *`locales`* 值匹配 `locale=`)组成，每个输入都没有或更多内部区域设置ID( *`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空 *`locId`* 值表示应 *`defaultString`* 返回（如果可用）。

有关详细信息，请参 `attribute::LocaleStrMap` 阅的说明。

## 翻译过程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

在上述示例翻译图和请求中 `/is/image/myCat/myItem?req=&locale=nl`，服务器首先在区域设置图 `nl`中查找“”。 匹配的条 `nl,N` 目表示，对于每 *`stringElement`*&#x200B;个条目， *`localizedString`* 应返回标 `^loc=N^` 有的条目。 如果 *`localizationToken`* 中不存在此值， *`stringElement`*&#x200B;则返回空值。

假设for包含 `catalog::UserData` 以 `myCat/myItem` 下内容（为了清晰起见，插入了换行符）:

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

服务器将返回以下内容以响应示例请求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知区域设置 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中， `attribute::LocaleStrMap` 有一个值为空的条 *`locale`* 目。 服务器使用此条目处理翻译图 `locale=` 中未明确指定的所有值。

示例翻译图指定在这种情况下，应 *`defaultString`* 当返回（如果有）。 因此，如果将此翻译图应用于请求，将返回以下内容 `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 示例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**语系**

多个 *`locId`* 值可以与翻译图中的每 *`locale`* 个值相关联。 这允许支持特定国家或地区的变体（例如，美国英语与英国英语）进行选择，同时处理大多数具有通用基本区域设置的内容（例如，国际英语）。 *`stringElements`*

对于我们的示例，我们希望添加对美国特定英语( ` *`locId`* EUS`)和英国特定英语( ` *`locId`* EUK`)的支持，以支持偶尔的替代拼写。 如果EUK或EUS不存在，我们会回到E同样，奥地利特定的德语变体( `DAT`)可以在大部分时间返回普通德语(标 *`localizedStrings`* 有 `D`)时根据需要提供。

`attribute::LocaleStrMap` 会是这样的：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表介绍了某些代表性组合和组合 *`stringElement`* 的输 *`locale`* 出：

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>输出字符串 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> “loc=E”“英语”“loc=D”“德语” </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> “loc”=“E”“loc”=“UK”-“英语”“loc”=“D”“德语”“loc”=“DAT”“奥地利” </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>英语 </p> <p>德文 </p> <p>奥地利语 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 请注意，在此示例中， <span class="varname"> locId </span> DDE在属性：:LocaleStrMap中不存在，因此，不会返回与此locId关联的子 <span class="codeph"> 字 </span><span class="varname"></span> 符串。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>美国——英语 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

