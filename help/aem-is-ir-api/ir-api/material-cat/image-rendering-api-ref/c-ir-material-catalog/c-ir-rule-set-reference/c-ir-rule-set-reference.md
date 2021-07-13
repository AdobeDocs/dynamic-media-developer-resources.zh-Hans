---
description: 图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# 规则集引用{#rule-set-reference}

图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

预处理规则集合（*规则集*）可以附加到材料目录或默认目录。 仅当请求未附加特定材料目录时，默认目录中的规则才适用。

请求预处理规则可以在请求的路径和查询部分被服务器的请求解析器处理之前修改它们，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些目录属性，以及将服务限制为特定客户端IP地址。

规则集将存储为XML文档文件。 必须在`attribute::RuleSetFile`中指定规则集文件的相对或绝对路径。

## 通用结构 {#section-74faaee27fc543a2ab4a306f3a03674e}

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

有效的规则集XML文件中始终需要`<?xml>`、`<!DOCTYPE>`和`<ruleset>`元素，即使未定义实际规则也是如此。

允许使用一个包含任意数量的`<rule>`元素的`<ruleset>`元素。

预处理规则文件的内容区分大小写。

## URL预处理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在进行任何其他处理之前，将部分解析传入的HTTP请求，以确定应应用哪些材料目录。 在识别目录后，将应用选定目录（或默认目录，如果未识别特定目录）的规则集。

按照与`<expression>`元素(*`expression`*)的内容匹配的指定顺序搜索`<rule>`元素。

如果`<rule>`匹配，则应用可选的&#x200B;*`substitution`*，并将修改的请求字符串传递到服务器的请求解析器，以进行正常处理。

如果在达到`<ruleset>`的结尾时未成功匹配，则该请求将被传递到解析器，而无需进行修改。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

可以使用`<rule>`元素的`OnMatch`属性修改默认行为。 `OnMatch` 可设置 `break` 为（默认）、 `continue`或  `error.`

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
   <td colname="col2"> <p>在应用此规则的替换后，规则处理将立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>将应用替换，并且处理会继续执行下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>规则处理会立即终止，并且“请求被拒绝”响应状态会返回给客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以选择定义在成功匹配并设置规则时覆盖相应目录属 `OnMatch="break"` 性的属性。如果设置了`OnMatch="continue"`，则不应用任何属性。 有关可使用规则控制的属性列表，请参阅`<rule>`的描述。

## 正则表达式 {#section-4d326507b52544b0960a9a5f303e3fe6}

简单的字符串匹配适用于非常基本的应用程序，但大多数情况下都需要正则表达式。 虽然正则表达式是行业标准，但具体实施因实例而异。

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 包介绍了图像服务使用的特定正则表达式实施。

## 捕获的子字符串 {#section-8057cd65d48949ffb6a50e929bd3688b}

为了便于进行复杂的URL修改，可以通过在表达式中使用圆括号(...)将子字符串括起来来捕获子字符串。 捕获的子字符串会根据前括号的位置按顺序从1开始编号。 捕获的子字符串可以使用&#x200B;*`$n`*&#x200B;插入到替换中，其中&#x200B;*`n`*&#x200B;是捕获的子字符串的序列号。

## 管理规则集文件 {#section-e8ce976b56404c009496426fd334d23d}

一个规则集文件可以附加到每个具有目录属性`attribute::RuleSetFile`的材料目录。 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的材料目录时才识别更改。 当启动或重新启动Platform Server时，以及修改或“触摸”主目录文件（具有[!DNL .ini]文件后缀）（更改文件日期）时，会发生这种情况。

## 示例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

规则集示例在图像提供文档的图像目录引用的相应部分中提供。

## 另请参阅 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
