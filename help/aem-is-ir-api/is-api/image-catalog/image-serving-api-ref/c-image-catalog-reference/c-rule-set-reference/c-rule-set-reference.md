---
description: 图像服务支持基于规则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# 规则集引用{#rule-set-reference}

图像服务支持基于规则表达式匹配和替换规则的简单请求预处理机制。

可以将预处理规则集合（*规则集*）附加到图像目录或默认目录。 仅当请求未标识特定主图像目录时，默认目录中的规则才适用。

请求预处理规则可以在请求的路径和查询部分由平台服务器的分析器处理之前对其进行修改，包括操作路径、添加命令、更改命令值以及应用模板或宏。 规则还可以用于配置和覆盖某些安全功能，这些功能通常仅通过目录属性进行控制，例如请求模糊处理、水标记以及将服务限制为特定客户端IP地址。

规则集存储为XML文档文件。 必须在`attribute::RuleSetFile`中指定规则集文件的相对或绝对路径。

## 常规结构{#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

有效规则集XML文件中始终需要`<?xml>`和`<ruleset>`元素，即使未定义任何实际规则也是如此。

允许使用一个包含任意数量`<rule>`元素的`<ruleset>`元素。

预处理规则文件的内容区分大小写。

## 规则集验证{#section-d8d101a0b4d74580835e37d128d05567}

目录文件夹中提供了[!DNL RuleSet.xsd]的副本，在将规则集文件注册到[!DNL catalog.ini]文件之前，应使用它验证该规则集文件。 请注意，图像服务使用[!DNL RuleSet.xsd]的内部副本进行验证。

## URL预处理{#section-2c09a2d79ada46b994857c6a7fb4c13a}

在进行任何其他处理之前，将部分分析传入的HTTP请求，以确定应应用哪个图像目录。 标识目录后，将应用选定目录（或默认目录，如果未标识特定目录）的规则集。

按为与`<expression>`元素(*`expression`*)的内容匹配而指定的顺序搜索`<rule>`元素。

如果`<rule>`匹配，则应用可选&#x200B;*`substitution`*，并将修改后的请求字符串传递给服务器的请求分析器以进行正常处理。

如果到达`<ruleset>`末尾时未成功匹配，则将请求传递给分析器，而不进行修改。

## OnMatch属性{#section-ed952fa55d99422db0ee68a2b9d395d3}

可以使用`<rule>`元素的`OnMatch`属性修改默认行为。 `OnMatch` 可以设置为 `break` （默认）、 `continue`或 `error`。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>元素和属性</b> </th> 
   <th class="entry"> <b>发生匹配时的行为</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>在应用此规则的替代后，规则处理立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>将应用替代，处理将继续使用下一条规则。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>规则处理会立即终止，并且“请求已拒绝”响应状态会返回给客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性{#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` elements可以选择定义在规则成功匹配时覆盖相应目录属性的属性。如果多个匹配规则设置了相同的属性，则最后一个规则优先。 有关可以使用规则控制的属性的列表，请参阅` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`元素的说明。

## 常规表达式{#section-3f77bb9a265147b38c645f63ab1bad8b}

简单的字符串匹配适用于非常基本的应用程序，但大多数情况下都需要常规表达式。 虽然常规表达式是行业标准，但具体实施因实例而异。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 介绍图像服务使用的特定常规表达式实现。

## 捕获的子字符串{#section-066e659406d5403599cd26ae35e80d68}

为了便于复杂的URL修改，可以在表达式中捕获子字符串，方法是将子字符串括在括号(...)中。 捕获的子字符串根据前括号的位置按顺序从1开始进行编号。 捕获的子字符串可以使用` $ *`n`*`插入到替换中，其中&#x200B;*`n`*&#x200B;是捕获的子字符串的序列号。

## 管理规则集文件{#section-0598a608e4044bb4805fe93ceebe10a9}

一个规则集文件可以附加到每个具有目录属性`attribute::RuleSetFile`的图像目录。 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的图像目录时识别更改。 当平台服务器启动或重新启动时，以及每当具有[!DNL .ini]文件后缀的主目录文件被修改或“触及”以更改文件日期时，都会发生此重新加载。

## 示例 {#section-aa769437d967459299b83a4bf34fe924}

**示例A.定** 义一个规则，如果图像名称的后缀为“”，则该规则会增加图像质量 [!DNL _hg]设置：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

规则表达式在URL字符串末尾指定“ [!DNL _hg]”的不区分大小写匹配。 后缀将替换为更改图像质量设置的指定查询字符串。 请注意，替换字符串中的`?`字符会转义，因为这是常规表达式中的特殊字符。

>[!NOTE]
>
>和号字符所需的编码。 或者，替换字符串可以包含在CDATA块中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**示例B.特** 定Web应用程序不允许查询字符串。定义将尾随路径元素`small`、`medium`或`large`转换为模板的规则，使用路径的其余部分作为图像名称。 例如，`myCat/myImage/small`将转换为`myCat/smallTemplate?src=myCat/myImage`。

我们可以使用子字符串来重构请求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另请参阅 {#section-9b748e7c5cff4759a70f96657bd43352}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
