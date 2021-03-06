---
title: initialFrame
description: 所有查看器通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# initialFrame{#initialframe}

所有查看器通用的参数。

>[!NOTE]
>
>此命令不适用于视频图像查看器。

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定查看器在加载时显示的从零开始的帧索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>当设备为纵向方向时，跨页中页面的从零开始的索引。 对于“从左到右”环境，<span class="codeph"> 0</span>表示“left page”，<span class="codeph"> 1</span>表示“right page”。 对于“从右到左”的环境，情况正好相反：<span class="codeph"> 0</span>表示“right page”，<span class="codeph"> 1</span>表示“left page”。 </p> <p>如果未指定，则默认情况下使用<span class="codeph"> 0</span>。 在设备处于横向位置时忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

没有默认设置。

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
