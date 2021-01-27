---
description: 查看器在主视图上显示搜索结果区域以突出显示在目录中找到的单词或短语。
seo-description: 查看器在主视图上显示搜索结果区域以突出显示在目录中找到的单词或短语。
seo-title: 搜索效果
solution: Experience Manager
title: 搜索效果
topic: Dynamic Media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 搜索效果{#search-effect}

查看器在主视图上显示搜索结果区域以突出显示在目录中找到的单词或短语。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

搜索结果区域的外观由以下CSS类选择器控制：

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p>搜索结果区域的背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要设置具有半透明黄色填充的搜索结果区域：

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

