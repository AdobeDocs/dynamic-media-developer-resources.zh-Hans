---
title: 文本字符串本地化
description: 文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 3%

---

# 文本字符串本地化{#text-string-localization}

文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。

服务器向客户端返回与指定的区域设置匹配的表示法 `locale=`，避免客户端本地化，并允许应用程序通过发送适当的区域设置来切换区域设置 `locale=` IS文本请求的值。

## 范围 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文本字符串本地化应用于包括本地化令牌的所有字符串元素 ` ^loc= *`locId`*^` 在下列目录字段中：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目录字段</b> </th> 
   <th class="entry"> <b>字段中的字符串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：图像集 </span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素（由分隔符“，”“；”“：”和/或字段的开始/结束位置的任何组合分隔）。 </p> <p> A <span class="codeph"> 0xrrggbb </span> 可本地化字段开头的颜色值将从本地化中排除，无需修改即可传递。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Map </span> </p> </td> 
   <td> <p>任何单引号或双引号属性值，但 <span class="codeph"> 颜色= </span> 和 <span class="codeph"> 形状= </span> 属性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：目标 </span> </p> </td> 
   <td> <p>任何值 <span class="codeph"> 目标。*.label </span> 和 <span class="codeph"> 目标。*.userdata </span> 属性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字符串语法 {#section-d12320edf300409f8e17565b143acafc}

启用本地化 *`string`* 图像目录中的元素由一个或多个本地化的字符串组成，每个字符串前面都有一个本地化令牌。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultstring </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedstring </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locstr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>的内部区域设置ID <span class="varname"> localizedstring </span> 关注此 <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedstring </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化的字符串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultstring </span> </span> </p> </td> 
  <td class="stentry"> <p>用于未知区域设置的字符串。 </p> </td> 
 </tr> 
</table>

此 *`locId`* 必须为ASCII并且不得包含“^”。

“^”可能出现在具有或不具有HTTP编码的子字符串中的任何位置。 服务器与整个 *`localizationToken`* `^loc=locId^` 用于分隔子字符串的模式。

此 *`stringElements`*，其中至少不包含一个 *`localizationToken`*&#x200B;不考虑本地化。

## 翻译图 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定义服务器用于确定哪个规则所使用的规则 *`localizedStrings`* 以返回客户端。 它由输入列表组成 *`locales`* (匹配指定的值 `locale=`)，每个区域设置没有内部区域设置ID或具有多个内部区域设置ID ( *`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空 *`locId`* 值指示 *`defaultString`* 应该返回（如果可用）。

请参阅的说明 `attribute::LocaleStrMap` 以了解详细信息。

## 翻译过程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

给定上面的示例翻译图和请求 `/is/image/myCat/myItem?req=&locale=nl`，服务器将首先查找&quot; `nl`”的区域设置映射中。 匹配的条目 `nl,N` 表示对于每个 *`stringElement`*， *`localizedString`* 已标记 `^loc=N^` 应该被退回 如果此 *`localizationToken`* 中不存在 *`stringElement`*，则返回空值。

比如说 `catalog::UserData` 对象 `myCat/myItem` 包含以下内容（为清楚起见，插入了换行符）：

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

服务器将返回以下内容以响应示例请求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知区域设置 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中， `attribute::LocaleStrMap` 具有包含空的条目 *`locale`* 值。 服务器使用此条目处理所有 `locale=` 在翻译映射中未另外显式指定的值。

示例翻译映射指定，在这种情况下， *`defaultString`* 应该返回（如果可用）。 因此，如果此翻译映射应用于请求，则会返回以下内容 `/is/image/myCat/myItem?req=&locale=ja`：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 示例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**语言系列**

多个 *`locId`* 值可以与每个 *`locale`* 在翻译图中。 原因是它允许为选定的项目支持特定于国家或地区的变体（例如，美国英语与英国英语） *`stringElements`* 处理大多数具有通用基本语言环境（例如，国际英语）的内容时。

例如，添加了对特定于美国的英语( `*`locId`* EUS`)和英国特定英语( `*`locId`* EUK`)，以支持偶尔的替代拼写。 如果EUK或EUS不存在，则它回退到E。同样，奥地利特定的德语变体( `DAT`)在返回常用德语时可以在需要时使用 *`localizedStrings`* (标记为 `D`)。

此 `attribute::LocaleStrMap` 将如下所示：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表描述了某些代表的输出 *`stringElement`* 和 *`locale`* 组合：

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^德语 </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Audiential </span> </p> </td> 
   <td> <p> en， en_us </p> <p> en_uk </p> <p> de， de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>UK — 英语 </p> <p>德文 </p> <p>奥地利语 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 在本例中， <span class="varname"> locId </span> DDE不存在于 <span class="codeph"> attribute：：LocaleStrMap </span>，因此是与此关联的子字符串 <span class="varname"> locId </span> 不会返回。 </p> </td> 
   <td> <p> en， en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>美式英语 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
