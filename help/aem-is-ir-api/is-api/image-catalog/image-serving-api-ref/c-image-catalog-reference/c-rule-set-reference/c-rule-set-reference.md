---
description: 图像服务支持基于正则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# 规则集引用{#rule-set-reference}

图像服务支持基于正则表达式匹配和替换规则的简单请求预处理机制。

预处理规则的集合(*规则集*)可以附加到图像目录或默认目录。 仅当请求未标识特定的主图像目录时，才应用默认目录中的规则。

请求预处理规则可以在处理请求之前修改请求的路径和查询部分 [!DNL Platform Server]的解析器，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些安全功能，这些功能通常仅由目录属性控制，例如请求模糊处理、水标记，以及将服务限制到特定客户端IP地址。

规则集存储为XML文档文件。 必须在以下位置指定规则集文件的相对路径或绝对路径： `attribute::RuleSetFile`.

## 常规结构 {#section-8bcbd91ea8a946f28051bde8ad21827f}

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

此 `<?xml>` 和 `<ruleset>` 有效规则集XML文件中始终需要元素，即使未定义实际规则也是如此。

一个 `<ruleset>` 包含任意数量的元素 `<rule>` 允许使用元素。

预处理规则文件的内容区分大小写。

## 规则集验证 {#section-d8d101a0b4d74580835e37d128d05567}

副本 [!DNL RuleSet.xsd] 在目录文件夹中提供，并且应该用于在中注册规则集文件之前验证该文件 [!DNL catalog.ini] 文件。 请注意，图像服务使用内部副本 [!DNL RuleSet.xsd] 以进行验证。

## URL预处理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

在任何其他处理之前，都会部分解析传入的HTTP请求，以确定应应用哪个图像目录。 标识目录后，将应用选定目录（或默认目录，如果未标识特定目录）的规则集。

此 `<rule>` 元素将按照为匹配项指定的顺序进行搜索，匹配项的内容为 `<expression>` 元素( *`expression`*)。

如果 `<rule>` 匹配，可选 *`substitution`* ，修改后的请求字符串将传递到服务器的请求分析器以进行正常处理。

如果在结束日期时没有成功匹配，则 `<ruleset>` 到达时，请求将传递到解析器而不进行修改。

## OnMatch属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

默认行为可修改为 `OnMatch` 的属性 `<rule>` 元素。 `OnMatch` 可以设置为 `break` （默认）， `continue`，或 `error`.

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
   <td> <p>应用此规则的替换后，规则处理将立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>将应用替换，并继续处理下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>规则处理会立即终止，并且会将“请求被拒绝”响应状态返回到客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-3f1e33a65c5346d1b4a69958c61432f3}

此 `rule` element可以选择在成功匹配规则时定义覆盖相应目录属性的属性。 如果多个匹配的规则设置了相同的属性，则最后一个规则优先。 参见 [规则](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 可以使用规则控制的属性列表的元素。

## 正则表达式 {#section-3f77bb9a265147b38c645f63ab1bad8b}

简单字符串匹配适用于非常基本的应用程序，但在大多数情况下都需要正则表达式。 虽然正则表达式是行业标准，但具体的实施因实例而异。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述图像服务使用的特定正则表达式实施。

## 捕获的子字符串 {#section-066e659406d5403599cd26ae35e80d68}

为了便于修改复杂的URL，可通过用圆括号(...)括住子字符串，从而在表达式中捕获子字符串。 捕获的子字符串根据前导圆括号的位置从1开始按顺序编号。 可以使用将捕获的子字符串插入到替换中 ` $ *`n`*`，其中 *`n`* 是捕获的子字符串的序列号。

## 管理规则集文件 {#section-0598a608e4044bb4805fe93ceebe10a9}

一个规则集文件可以附加到每个具有目录属性的图像目录 `attribute::RuleSetFile`. 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的图像目录时识别更改。 当平台服务器启动或重新启动时，以及每当主目录文件(具有 [!DNL .ini] 文件后缀，修改或“接触”以更改文件日期。

## 示例 {#section-aa769437d967459299b83a4bf34fe924}

**示例A.** 如果图像名称具有后缀&#39;&#39;&#39;，则定义增加图像质量设置的规则 [!DNL _hg]“：

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

规则表达式指定&#39;&#39;的匹配项（不区分大小写） [!DNL _hg]”作为前缀。 后缀被替换成更改图像质量设置的指定查询字符串。 请注意 `?` 替换字符串中的字符会被转义，因为这是正则表达式中的特殊字符。

>[!NOTE]
>
>&amp;字符的必需编码。 或者，可以将替换字符串包含在CDATA块中：

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**示例B.** 特定的Web应用程序不允许查询字符串。 定义翻译尾随路径元素的规则 `small`， `medium`，或 `large` 到模板，使用路径的其余部分作为图像名称。 例如， `myCat/myImage/small` 将转换为 `myCat/smallTemplate?src=myCat/myImage`.

我们可以使用子字符串来重构请求：

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 另请参阅 {#section-9b748e7c5cff4759a70f96657bd43352}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
