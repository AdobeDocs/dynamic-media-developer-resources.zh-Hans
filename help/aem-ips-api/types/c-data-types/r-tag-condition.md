---
description: 定义标记字段的搜索条件。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 7%

---


# TagCondition{#tagcondition}

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
   <td colname="col3">取决于标记字段类型以及是否使用value或valueArray字段。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">如果传递了<span class="codeph">值</span>，则<span class="codeph"> op</span>必须是字符串常数Matches。 该条件匹配与标记值关联的任何资产。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">如果传递了<span class="codeph"> valueArray</span>，则op字段可以是单个或多值标记字段的常量<span class="codeph"> MatchesAny</span>。 <span class="codeph"> MatchesAny</span>条件匹配与<span class="codeph"> valueArray</span>中至少一个标记值关联的任何资产。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">对于多值标记字段，op字段可设置为具有<span class="codeph"> valueArray</span>字段的常量<span class="codeph"> MatchesAll</span>。 在这种情况下，该条件仅匹配与<span class="codeph"> valueArray</span>中所有标记值（可能还有其他标记值）关联的资产。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 匹配值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 多个匹配值。 </td> 
  </tr> 
 </tbody> 
</table>

