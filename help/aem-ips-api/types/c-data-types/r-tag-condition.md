---
description: 定义标记字段的搜索条件。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 7%

---

# [!DNL TagCondition]{#tagcondition}

定义标记字段的搜索条件。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 标记字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">取决于标记字段类型以及使用的是value还是valueArray字段。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果 <span class="codeph"> 值</span> 通过， <span class="codeph"> 操作</span> 必须为字符串常量Matches。 条件匹配与标记值关联的任何资源。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果 <span class="codeph"> valueArray</span> 传递，操作字段可以是常量 <span class="codeph"> MatchesAny</span> 用于单值或多值标记字段。 A <span class="codeph"> MatchesAny</span> 条件匹配与中的至少一个标记值关联的任何资源 <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">对于多值标记字段，可将op字段设置为常量 <span class="codeph"> MatchesAll</span> 使用 <span class="codeph"> valueArray</span> 字段。 在这种情况下，条件仅匹配与中的所有标记值关联的资产。 <span class="codeph"> valueArray</span> （可能是在其他标记值之外）。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 匹配值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：StringArray</span> </td> 
   <td colname="col3"> 多个匹配值。 </td> 
  </tr> 
 </tbody> 
</table>
