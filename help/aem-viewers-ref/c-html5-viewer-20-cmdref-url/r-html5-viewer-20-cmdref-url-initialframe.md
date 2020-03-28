---
description: 所有查看器通用的参数。
seo-description: 所有查看器通用的参数。
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span></span> </p> </td> 
   <td colname="col2"> <p> 指定查看器在加载时显示的从零开始的帧索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>当设备纵向时，跨页中从零开始的页面索引。 在“从左至右”环境中， <span class="codeph"> 0表示</span> “左页”, <span class="codeph"> 1表示“右页</span> ”。 在“从右到左”中，情况正好相反： <span class="codeph"> 0表示</span> “右页”, <span class="codeph"> 1表示</span> “左页”。 </p> <p>如果未指定，则 <span class="codeph"> 默认情况下</span> ，假定为0。 设备横向时忽略。 </p> </td> 
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

