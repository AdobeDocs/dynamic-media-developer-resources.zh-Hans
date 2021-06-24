---
description: 文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。
solution: Experience Manager
title: 文本字符串本地化
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 3%

---

# 文本字符串本地化{#text-string-localization}

文本字符串本地化允许图像目录包含同一字符串值的多个特定于区域设置的表示形式。

服务器将与指定的`locale=`区域设置匹配的表示形式返回到客户端，从而避免了客户端本地化，并且允许应用程序只需通过IS文本请求发送适当的`locale=`值即可切换区域设置。

## 范围 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

文本字符串本地化将应用于以下目录字段中包含本地化令牌` ^loc= *`locId`*^`的所有字符串元素：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>目录字段</b> </th> 
   <th class="entry"> <b>字段中的字符串元素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>包含可翻译字符串的任何子元素（由分隔符“，”“；”“：”和/或字段开头/结尾的任意组合分隔）。 </p> <p> 本地化字段开头的<span class="codeph"> 0xrrggbb </span>颜色值将从本地化中排除，并且无需修改即可传递。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：:Map  </span> </p> </td> 
   <td> <p>任何单引号或双引号属性值，但<span class="codeph"> coords= </span>和<span class="codeph"> shape= </span>属性的值除外。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 目录：：目标  </span> </p> </td> 
   <td> <p>任意<span class="codeph">目标的值。*.label </span>和<span class="codeph">目标。*.userdata </span>属性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>任何属性的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 字符串语法 {#section-d12320edf300409f8e17565b143acafc}

图像目录中启用了本地化的&#x200B;*`string`*&#x200B;元素由一个或多个本地化字符串组成，每个字符串前面都有一个本地化令牌。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>此<span class="varname"> localizationToken </span>之后<span class="varname"> localizedString </span>的内部区域设置ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>本地化字符串。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>用于未知区域设置的字符串。 </p> </td> 
 </tr> 
</table>

*`locId`* 必须为ASCII，且不能包含“^”。

“^”可能位于包含或不包含HTTP编码的子字符串中的任意位置。 服务器与整个&#x200B;*`localizationToken`* `^loc=locId^`模式匹配以分隔子字符串。

*`stringElements`* 不会考虑将其中至少一个 *`localizationToken`* 不包含在本地。

## 翻译图 {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` 定义服务器用来确定要返回给客 *`localizedStrings`* 户端的规则。它包含输入&#x200B;*`locales`*（与`locale=`指定的值匹配）列表，每个输入都没有或更多内部区域设置ID(*`locId`*)。 例如：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空的&#x200B;*`locId`*&#x200B;值表示应返回&#x200B;*`defaultString`*（如果可用）。

有关详细信息，请参阅`attribute::LocaleStrMap`的描述。

## 翻译过程 {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

假定上面的示例翻译映射和请求`/is/image/myCat/myItem?req=&locale=nl`，服务器首先在区域设置映射中查找“ `nl`”。 匹配的条目`nl,N`表示对于每个&#x200B;*`stringElement`*，应返回标有`^loc=N^`的&#x200B;*`localizedString`*。 如果&#x200B;*`localizationToken`*&#x200B;不在&#x200B;*`stringElement`*&#x200B;中，则返回空值。

假设`myCat/myItem`的`catalog::UserData`包含以下内容（为清楚起见，插入了换行符）：

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

服务器将返回以下响应示例请求：

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 未知区域设置 {#section-26dfeefbd60345de94bbfeaaf7741223}

在上例中，`attribute::LocaleStrMap`有一个值为空的条目。 *`locale`*&#x200B;服务器使用此条目来处理所有在翻译映射中未明确指定的`locale=`值。

示例翻译图指定，在这种情况下，应返回&#x200B;*`defaultString`*（如果可用）。 因此，如果将此翻译映射应用于请求`/is/image/myCat/myItem?req=&locale=ja`，则将返回以下内容：

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 示例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**语言系列**

多个&#x200B;*`locId`*&#x200B;值可能与翻译映射中的每个&#x200B;*`locale`*&#x200B;值相关联。 这允许支持特定于国家/地区或地区的变体（例如，美国英语与英国英语）来选择&#x200B;*`stringElements`*，同时处理大多数具有相同基本区域设置（例如，国际英语）的内容。

例如，我们希望添加对特定于美国的英语(`*`locId`* EUS`)和特定于英国的英语(`*`locId`* EUK`)的支持，以支持偶尔的替代拼写。 如果EUK或EUS不存在，我们将回退到E。同样，在大多数情况下返回常用德语&#x200B;*`localizedStrings`*（标有`D`）时，可以根据需要提供特定于奥地利的德语变体(`DAT`)。

`attribute::LocaleStrMap` 会如下所示：

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

下表介绍了一些代表性的&#x200B;*`stringElement`*&#x200B;和&#x200B;*`locale`*&#x200B;组合的输出：

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en， en_us </p> <p> en_uk </p> <p> de， de_de </p> <p>de_at </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>英语 </p> <p>德文 </p> <p>奥地利 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^english^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> 请注意，在此示例中，<span class="varname"> locId </span>属性中不存在<span class="codeph"> DDE::LocaleStrMap </span>，因此永远不会返回与此<span class="varname"> locId </span>关联的子字符串。 </p> </td> 
   <td> <p> en， en_uk </p> <p> en_us </p> <p> de， de_at， de_de </p> <p>所有其他 </p> </td> 
   <td> <p>英文 </p> <p>美式英语 </p> <p>德文 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
