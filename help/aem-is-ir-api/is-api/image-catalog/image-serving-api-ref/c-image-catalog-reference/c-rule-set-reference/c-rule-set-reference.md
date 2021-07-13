---
description: 图像服务支持基于正则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# 规则集引用{#rule-set-reference}

图像服务支持基于正则表达式匹配和替换规则的简单请求预处理机制。

预处理规则集合（*规则集*）可以附加到图像目录或默认目录。 仅当请求未标识特定的主图像目录时，才应用默认目录中的规则。

请求预处理规则可以在请求的路径和查询部分由Platform Server的解析器处理之前对其进行修改，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些安全功能，这些功能通常仅通过目录属性来控制，例如请求模糊处理、水标记，以及将服务限制为特定的客户端IP地址。

规则集将存储为XML文档文件。 必须在`attribute::RuleSetFile`中指定规则集文件的相对或绝对路径。

## 通用结构 {#section-8bcbd91ea8a946f28051bde8ad21827f}

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

有效的规则集XML文件中始终需要`<?xml>`和`<ruleset>`元素，即使未定义实际规则也是如此。

允许使用一个包含任意数量的`<rule>`元素的`<ruleset>`元素。

预处理规则文件的内容区分大小写。

## 规则集验证 {#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd]的副本在目录文件夹中提供，在将规则集文件注册到[!DNL catalog.ini]文件之前，应使用该副本来验证该规则集文件。 请注意，图像提供使用[!DNL RuleSet.xsd]的内部副本进行验证。

## URL预处理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在进行任何其他处理之前，会部分解析传入的HTTP请求，以确定应应用哪个图像目录。 在识别目录后，将应用选定目录（或默认目录，如果未识别特定目录）的规则集。

按照与`<expression>`元素(*`expression`*)的内容匹配的指定顺序搜索`<rule>`元素。

如果`<rule>`匹配，则应用可选的&#x200B;*`substitution`*，并将修改的请求字符串传递到服务器的请求解析器，以进行正常处理。

如果在达到`<ruleset>`的结尾时未成功匹配，则该请求将被传递到解析器，而无需进行修改。

## OnMatch属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

可以使用`<rule>`元素的`OnMatch`属性修改默认行为。 `OnMatch` 可设置为 `break` （默认）、 `continue`或 `error`。

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
   <td> <p>在应用此规则的替换后，规则处理将立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>将应用替换，并且处理会继续执行下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>规则处理会立即终止，并且“请求被拒绝”响应状态会返回给客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 元素可以选择定义在规则成功匹配时覆盖相应目录属性的属性。如果多个匹配的规则设置了相同的属性，则最后一个规则将占上风。 有关可使用规则控制的属性列表，请参阅` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`元素的描述。

## 正则表达式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

简单的字符串匹配适用于非常基本的应用程序，但大多数情况下都需要正则表达式。 虽然正则表达式是行业标准，但具体实施因实例而异。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述图像服务使用的特定正则表达式实施。

## 捕获的子字符串 {#section-066e659406d5403599cd26ae35e80d68}

为了便于进行复杂的URL修改，可以通过在表达式中使用圆括号(...)将子字符串括起来来捕获子字符串。 捕获的子字符串会根据前括号的位置按顺序从1开始编号。 捕获的子字符串可以使用` $ *`n`*`插入到替换中，其中&#x200B;*`n`*&#x200B;是捕获的子字符串的序列号。

## 管理规则集文件 {#section-0598a608e4044bb4805fe93ceebe10a9}

每个具有目录属性`attribute::RuleSetFile`的图像目录可附加一个规则集文件。 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的图像目录时才会识别更改。 当平台服务器启动或重新启动时，以及当具有[!DNL .ini]文件后缀的主目录文件被修改或“触摸”以更改文件日期时，会进行此重新加载。

## 示例 {#section-aa769437d967459299b83a4bf34fe924}

**示例A.** 定义一个规则，当图像名称的后缀为“ [!DNL _hg]”时，该规则会提高图像质量设置：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

规则表达式在URL字符串的末尾指定“ [!DNL _hg]”（不区分大小写）匹配。 后缀将替换为更改图像质量设置的指定查询字符串。 请注意，替换字符串中的`?`字符会转义，因为这是正则表达式中的特殊字符。

>[!NOTE]
>
>与号字符所需的编码。 或者，替换字符串可以包含在CDATA块中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**示例B.** 特定Web应用程序不允许查询字符串。定义一个规则，该规则将尾随路径元素`small`、`medium`或`large`转换为模板，并使用路径的其余部分作为图像名称。 例如， `myCat/myImage/small`将转换为`myCat/smallTemplate?src=myCat/myImage`。

我们可以使用子字符串来重构请求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另请参阅 {#section-9b748e7c5cff4759a70f96657bd43352}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
