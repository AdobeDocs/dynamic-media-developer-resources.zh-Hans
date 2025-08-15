---
description: 图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# 规则集引用{#rule-set-reference}

图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

预处理规则集合（*规则集*）可以附加到材料目录或默认目录。 仅当请求未附加特定材质目录时，默认目录中的规则才适用。

请求预处理规则可以在请求的路径和查询部分被服务器的请求解析器处理之前对其进行修改，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些目录属性，以及将服务限制到特定客户端IP地址。

规则集存储为XML文档文件。 必须在`attribute::RuleSetFile`中指定规则集文件的相对路径或绝对路径。

## 常规结构 {#section-74faaee27fc543a2ab4a306f3a03674e}

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

有效规则集XML文件中始终需要`<?xml>`、`<!DOCTYPE>`和`<ruleset>`元素，即使未定义实际规则也是如此。

允许一个包含任意数量的`<ruleset>`元素的`<rule>`元素。

预处理规则文件的内容区分大小写。

## URL预处理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在任何其他处理之前，传入HTTP请求会被部分解析，以确定应应用哪种材质目录。 标识目录后，将应用选定目录（如果没有标识特定目录，则为默认目录）的规则集。

`<rule>`元素按指定的顺序搜索，以查找与`<expression>`元素(*`expression`*)内容的匹配。

如果`<rule>`匹配，则应用可选的&#x200B;*`substitution`*，并将修改后的请求字符串传递到服务器的请求分析器以进行正常处理。

如果在到达`<ruleset>`的结尾时没有成功匹配，则请求将传递到分析器而不进行修改。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用`OnMatch`元素的`<rule>`属性修改默认行为。 `OnMatch`可以设置为`break`（默认）、`continue`或`error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元素和属性 </p> </th> 
   <th colname="col2" class="entry"> <p>发生匹配时的行为 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>应用此规则的替换之后，规则处理将立即终止。 默认。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;规则OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>将应用替换，并继续处理下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;规则OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>规则处理立即终止，并向客户端返回“请求被拒绝”响应状态。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

当规则成功匹配且设置了`<rule>`时，`OnMatch="break"`元素可以选择定义覆盖相应目录属性的属性。 如果设置了`OnMatch="continue"`，则不会应用任何属性。 有关可使用规则控制的属性列表，请参阅`<rule>`的说明。

## 正则表达式 {#section-4d326507b52544b0960a9a5f303e3fe6}

简单字符串匹配适用于非常基本的应用程序，但在大多数情况下都需要正则表达式。 虽然正则表达式是符合行业标准的，但具体的实施因实例而异。

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)描述了图像服务使用的特定正则表达式实现。

## 捕获的子字符串 {#section-8057cd65d48949ffb6a50e929bd3688b}

为了便于进行复杂的URL修改，可通过用圆括号(...)将子字符串括起来，从而在表达式中捕获子字符串。 捕获的子字符串根据前导圆括号的位置从1开始按顺序编号。 捕获的子字符串可以使用&#x200B;*`$n`*&#x200B;插入替换中，其中&#x200B;*`n`*&#x200B;是捕获的子字符串的序列号。

## 管理规则集文件 {#section-e8ce976b56404c009496426fd334d23d}

可以将一个规则集文件附加到具有目录属性`attribute::RuleSetFile`的每个材质目录。 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的材料目录时才识别更改。 当[!DNL Platform Server]启动或重新启动时，以及当主目录文件（具有[!DNL .ini]文件后缀）被修改或“接触”（更改文件日期）时，会发生这种情况。

## 示例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

规则集示例在图像服务文档的图像目录引用的相应部分中提供。

## 另请参阅 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
