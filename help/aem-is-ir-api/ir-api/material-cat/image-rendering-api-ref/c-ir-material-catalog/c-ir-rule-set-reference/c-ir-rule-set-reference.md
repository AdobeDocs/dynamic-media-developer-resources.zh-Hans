---
description: 图像渲染支持基于常规表达式匹配和替换规则的简单请求预处理机制。
seo-description: 图像渲染支持基于常规表达式匹配和替换规则的简单请求预处理机制。
seo-title: 规则集引用
solution: Experience Manager
title: 规则集引用
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 规则集引用{#rule-set-reference}

图像渲染支持基于常规表达式匹配和替换规则的简单请求预处理机制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

预处理规则集(规则集&#x200B;**)可以附加到材料目录或默认目录。 仅当请求未附加特定的材料目录时，默认目录中的规则才适用。

请求预处理规则可以在请求解析器处理请求之前修改路径和查询部分，包括操作路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些目录属性，以及将服务限制到特定客户端IP地址。

规则集存储为XML文档文件。 必须在中指定规则集文件的相对或绝对路径 `attribute::RuleSetFile`。

## 一般结构 {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

有效 `<?xml>``<!DOCTYPE>``<ruleset>` 的规则集XML文件中始终需要和元素，即使没有定义实际的规则。

允许 `<ruleset>` 一个包含任意数量的元 `<rule>` 素的元素。

预处理规则文件的内容区分大小写。

## URL预处理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在进行任何其他处理之前，将部分分析传入的HTTP请求，以确定应应用哪些材料目录。 在标识目录后，将应用选定目录（或默认目录，如果未标识特定目录）的规则集。

按 `<rule>` 照与元素()的内容匹配的指定顺序搜索 `<expression>` 元素( *`expression`*)。

如果匹 `<rule>` 配，则应用可选 *`substitution`* 请求字符串并将修改的请求字符串传递给服务器的请求分析器以进行正常处理。

如果到达结束时未成功匹配，则请 `<ruleset>` 求将传递给分析器，而无需修改。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用元素的属性修改 `OnMatch` 默认行 `<rule>` 为。 `OnMatch` 可以设置为 `break` （默认）、 `continue`或 `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元素和属性 </p> </th> 
   <th colname="col2" class="entry"> <p>匹配时的行为 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule onMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>规则处理在应用此规则的替换后立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule onMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>将应用替换，并且处理将继续执行下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>规则处理会立即终止，并且“请求已拒绝”响应状态会返回到客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以选择定义在规则成功匹配和设置时覆盖相应目录属性 `OnMatch="break"` 的属性。 如果设置了属性，则不 `OnMatch="continue"` 会应用任何属性。 请参阅的说明， `<rule>` 了解可以使用规则控制的属性列表。

## 常规表达式 {#section-4d326507b52544b0960a9a5f303e3fe6}

简单的字符串匹配适用于非常基本的应用程序，但大多数情况下都需要常规表达式。 虽然常规表达式是行业标准，但具体实施因实例而异。

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述图像服务使用的特定常规表达式实现。

## 捕获的子字符串 {#section-8057cd65d48949ffb6a50e929bd3688b}

为了便于复杂的URL修改，子字符串可以在表达式中通过用括号(...)括起子字符串来捕获。 捕获的子字符串根据前括号的位置以1开始按顺序编号。 捕获的子字符串可以使用插入替换中 *`$n`*，其中 *`n`* 是捕获的子字符串的序列号。

## 管理规则集文件 {#section-e8ce976b56404c009496426fd334d23d}

一个规则集文件可以附加到具有目录属性的每个材料目录 `attribute::RuleSetFile`。 虽然您可以随时编辑规则集文件，但图像服务器只有在重新加载关联的材料目录时才能识别所做的更改。 当启动或重新启动平台服务器时，以及每当主目录文件（具有文件后缀）被修改或“改动”（以更改文件日期）时，会发生这种情况。 [!DNL .ini]

## 示例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

规则集示例在图像服务文档的图像目录参考的相应部分中提供。

## 另请参阅 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
