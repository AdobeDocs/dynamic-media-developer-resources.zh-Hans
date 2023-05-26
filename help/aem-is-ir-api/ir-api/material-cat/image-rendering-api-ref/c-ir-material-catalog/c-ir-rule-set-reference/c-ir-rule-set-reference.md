---
description: 图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。
solution: Experience Manager
title: 规则集引用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# 规则集引用{#rule-set-reference}

图像渲染支持基于正则表达式匹配和替换规则的简单请求预处理机制。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

预处理规则的集合(*规则集*)可以附加到材料目录或默认目录。 仅当请求未附加特定材质目录时，才应用默认目录中的规则。

请求预处理规则可以在服务器的请求解析器处理请求之前修改请求的路径和查询部分，包括处理路径、添加命令、更改命令值以及应用模板或宏。 规则还可用于配置和覆盖某些目录属性，以及将服务限制到特定客户端IP地址。

规则集存储为XML文档文件。 必须在以下位置指定规则集文件的相对路径或绝对路径： `attribute::RuleSetFile`.

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

此 `<?xml>`， `<!DOCTYPE>` 和 `<ruleset>` 有效规则集XML文件中始终需要元素，即使未定义实际规则也是如此。

一个 `<ruleset>` 包含任意数量的元素 `<rule>` 允许使用元素。

预处理规则文件的内容区分大小写。

## URL预处理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

在任何其他处理之前，都会部分解析传入的HTTP请求，以确定应应用哪个材质目录。 标识目录后，将应用选定目录（或默认目录，如果未标识特定目录）的规则集。

此 `<rule>` 元素将按照为匹配项指定的顺序进行搜索，匹配项的内容为 `<expression>` 元素( *`expression`*)。

如果 `<rule>` 匹配，可选 *`substitution`* ，修改后的请求字符串将传递到服务器的请求分析器以进行正常处理。

如果在结束日期时没有成功匹配，则 `<ruleset>` 到达时，请求将传递到解析器而不进行修改。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

默认行为可修改为 `OnMatch` 的属性 `<rule>` 元素。 `OnMatch` 可以设置为 `break` （默认）， `continue`，或 `error.`

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
   <td colname="col2"> <p>应用此规则的替换后，规则处理将立即终止。 默认. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>将应用替换，并继续处理下一个规则。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>规则处理会立即终止，并且会将“请求被拒绝”响应状态返回到客户端。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 覆盖目录属性 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 元素可以选择性地定义属性，这些属性在规则成功匹配时覆盖相应的目录属性，并且 `OnMatch="break"` 设置。 在以下情况下不会应用任何属性： `OnMatch="continue"` 设置。 请参阅 `<rule>` 以获取可以使用规则控制的属性列表。

## 正则表达式 {#section-4d326507b52544b0960a9a5f303e3fe6}

简单字符串匹配适用于非常基本的应用程序，但在大多数情况下都需要正则表达式。 虽然正则表达式是行业标准，但具体的实施因实例而异。

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 描述图像服务使用的特定正则表达式实施。

## 捕获的子字符串 {#section-8057cd65d48949ffb6a50e929bd3688b}

为了便于修改复杂的URL，可通过用圆括号(...)括住子字符串，从而在表达式中捕获子字符串。 捕获的子字符串根据前导圆括号的位置从1开始按顺序编号。 可以使用将捕获的子字符串插入到替换中 *`$n`*，其中 *`n`* 是捕获的子字符串的序列号。

## 管理规则集文件 {#section-e8ce976b56404c009496426fd334d23d}

一个规则集文件可以附加到每个具有目录属性的材料目录 `attribute::RuleSetFile`. 虽然您可以随时编辑规则集文件，但图像服务器仅在重新加载关联的材料目录时识别更改。 此问题发生于 [!DNL Platform Server] 启动或重新启动以及每当主目录文件(具有 [!DNL .ini] 文件后缀)已被修改或“接触”（以更改文件日期）。

## 示例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

规则集示例在图像服务文档中的图像目录引用的相应部分中提供。

## 另请参阅 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[包java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
