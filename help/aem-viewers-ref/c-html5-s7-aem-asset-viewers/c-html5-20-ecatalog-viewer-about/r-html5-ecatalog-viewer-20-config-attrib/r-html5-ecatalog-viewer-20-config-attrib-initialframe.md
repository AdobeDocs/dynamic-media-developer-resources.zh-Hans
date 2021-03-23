---
description: 初始帧
solution: Experience Manager
title: 初始帧
uuid: edd95500-a83d-4012-8850-b41c06c4c9e8
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 8%

---


# InitialFrame{#initialframe}

` initialFrame= *`frame`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> 指定在加载查看器时显示的从零开始的跨页索引。 该索引与横向模式下跨页的索引匹配。 如果将查看器旋转为纵向，则查看器将显示由<span class="codeph"> frameIdx</span>指向的跨页中最左侧的页面。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-fc7c012c91d1419b8a5bb60d28e17327}

可选。

## 默认 {#section-bbc6ebad3af54fd79837515c270e6ddf}

`0`

## 示例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

在查看器URL中指定时。

```
initialFrame=2
```

