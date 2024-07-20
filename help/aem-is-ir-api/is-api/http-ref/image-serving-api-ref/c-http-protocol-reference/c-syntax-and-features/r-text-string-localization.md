---
title: 文本字符串本地化
description: 文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# 文本字符串本地化{#text-string-localization}

文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。

服务器将与`locale=`指定的区域设置匹配的表示返回到客户端，从而避免客户端本地化，并允许应用程序通过发送相应的`locale=`值和IS文本请求来切换区域设置。

## 范围 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文本字符串本地化应用于以下目录字段中包含本地化令牌` ^loc= *`locId`*^`的所有字符串元素：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目录字段</b> </th> 
   <th class="entry"> <b>字段中的字符串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">目录：：图像集</span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素（由分隔符“，”“；”“：”和/或字段的开始/结束位置的任何组合分隔）。 </p> <p> 可本地化字段开头的<span class="codeph"> 0xrrggbb </span>颜色值从本地化中排除，无需修改即可传递。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：映射</span> </p> </td> 
   <td> <p>任何单引号或双引号属性值，但<span class="codeph">坐标= </span>和<span class="codeph">形状= </span>属性的值除外。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：目标</span> </p> </td> 
   <td> <p>任何<span class="codeph">目标的值。*.label </span>和<span class="codeph">目标*.userdata </span>属性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">目录：：UserData </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字符串语法 {#section-d12320edf300409f8e17565b143acafc}

图像目录中启用了本地化的&#x200B;*`string`*&#x200B;元素由一个或多个本地化字符串组成，每个字符串前面都有一个本地化令牌。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">本地化令牌</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> localizedString </span>的内部区域设置ID位于此<span class="varname"> localizedToken </span>之后。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化的字符串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">默认字符串</span> </span> </p> </td> 
  <td class="stentry"> <p>用于未知区域设置的字符串。 </p> </td> 
 </tr> 
</table>

*`locId`*&#x200B;必须是ASCII格式，不能包括“^”。

“^”可能出现在具有或不具有HTTP编码的子字符串中的任何位置。 服务器将整个&#x200B;*`localizationToken`* `^loc=locId^`模式匹配为分隔子字符串。

*`stringElements`*&#x200B;不包含至少一个&#x200B;*`localizationToken`*，不考虑进行本地化。

## 翻译图 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap`定义服务器用于确定哪个&#x200B;*`localizedStrings`*&#x200B;返回到客户端的规则。 它包含输入&#x200B;*`locales`*&#x200B;的列表（与使用`locale=`指定的值匹配），每个列表均不含一个或多个内部区域设置ID ( *`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空&#x200B;*`locId`*&#x200B;值表示应返回&#x200B;*`defaultString`*（如果可用）。

有关详细信息，请参阅`attribute::LocaleStrMap`的说明。

## 翻译过程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

给定上面的示例翻译映射和请求`/is/image/myCat/myItem?req=&locale=nl`，服务器首先在区域设置映射中查找“`nl`”。 匹配的条目`nl,N`指示对于每个&#x200B;*`stringElement`*，应返回标记为`^loc=N^`的&#x200B;*`localizedString`*。 如果&#x200B;*`stringElement`*&#x200B;中不存在此&#x200B;*`localizationToken`*，则返回空值。

假设`myCat/myItem`的`catalog::UserData`包含以下内容（为清楚起见，插入了换行符）：

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

服务器将返回以下内容以响应示例请求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知区域设置 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中，`attribute::LocaleStrMap`有一个包含空&#x200B;*`locale`*&#x200B;值的条目。 服务器使用此条目处理翻译映射中未明确指定的所有`locale=`值。

示例翻译映射指定在这种情况下，应返回&#x200B;*`defaultString`*（如果可用）。 因此，如果将此翻译映射应用于请求`/is/image/myCat/myItem?req=&locale=ja`，则会返回以下内容：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 示例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**语言系列**

多个&#x200B;*`locId`*&#x200B;值可以与翻译映射中的每个&#x200B;*`locale`*&#x200B;关联。 原因在于，它允许为所选&#x200B;*`stringElements`*&#x200B;支持特定于国家或地区的变体（例如，美国英语与英国英语），同时处理大多数具有通用基本区域设置的内容（例如，国际英语）。

例如，添加了对特定于美国的英语(`*`locId`* EUS`)和特定于英国的英语(`*`locId`* EUK`)的支持，以支持偶尔的替代拼写。 如果EUK或EUS不存在，则它回退到E。同样，奥地利特定的德语变体(`DAT`)可以在大多数情况下返回通用德语&#x200B;*`localizedStrings`*（用`D`标记）时根据需要提供。

`attribute::LocaleStrMap`将如下所示：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表描述了某些代表&#x200B;*`stringElement`*&#x200B;和&#x200B;*`locale`*&#x200B;组合的输出：

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>区域设置</i> </th> 
   <th class="entry"> <p>输出字符串 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en， en_us， en_uk </p> <p> de， de_at， de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Audiential </span> </p> </td> 
   <td> <p> en， en_us </p> <p> en_uk </p> <p> de， de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>UK — 英语 </p> <p>德文 </p> <p>奥地利语 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> 对于此示例，<span class="varname"> locId </span> DDE在<span class="codeph">属性：：LocaleStrMap </span>中不存在，因此从不返回与此<span class="varname"> locId </span>关联的子字符串。 </p> </td> 
   <td> <p> en， en_uk </p> <p> en_us </p> <p> de， de_at， de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>美式英语 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
