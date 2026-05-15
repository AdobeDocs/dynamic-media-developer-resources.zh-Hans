---
title: 初始帧
description: 所有查看者通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: 'https://experienceleague.adobe.com/v4kG-OcDN3wmdHDClJHeLR8d2SNcMa5sRQo89Qwig4I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

---

# 初始帧{#initialframe}

所有查看者通用的参数。

>[!NOTE]
>
>此命令不适用于视频图像查看器。

` initialFrame= *`frameIdx`*[ *`，pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定查看器在加载时显示的从零开始的帧索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>当设备纵向时，跨页中页面的索引（从零开始）。 对于“从左至右”的环境，<span class="codeph"> 0</span>表示“左页”，<span class="codeph"> 1</span>表示“右页”。 对于“从右至左”的环境，则相反： <span class="codeph"> 0</span>表示“右页”，<span class="codeph"> 1</span>表示“左页”。 </p> <p>如果未指定，则默认情况下假定为<span class="codeph"> 0</span>。 当设备处于横向时忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无默认值。

## 示例： {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
