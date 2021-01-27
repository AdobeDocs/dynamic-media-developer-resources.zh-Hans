---
description: 所有查看器通用的参数。
seo-description: 所有查看器通用的参数。
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic Media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

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
   <td colname="col2"> <p>设备纵向时跨页中页面的从零开始的索引。 在“从左到右”环境<span class="codeph"> 0</span>表示“左页”,<span class="codeph"> 1</span>表示“右页”。 在“从右到左”中，情况恰恰相反：<span class="codeph"> 0</span>表示“right page”,<span class="codeph"> 1</span>表示“left page”。 </p> <p>如果未指定，则默认情况下假定<span class="codeph"> 0</span>。 设备横向时忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无默认值。

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

