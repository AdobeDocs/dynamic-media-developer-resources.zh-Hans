---
description: 如果将JavaScript™指定为响应格式，则回复数据的格式将解析为JavaScript™包含文件。
solution: Experience Manager
title: JavaScript™属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# JavaScript™属性{#javascript-properties}

如果将JavaScript™指定为响应格式，则回复数据的格式将解析为JavaScript™包含文件。

典型的JavaScript™属性响应具有以下常规结构：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可以为空。 每行开头和结尾以及=分隔符之前和之后的空格是可选的。 所有值都用单引号括起来。 字符串中的单引号使用两个连续的单引号进行转义。

要分析JavaScript™属性响应，必须在加载属性文件之前创建响应中引用的任何对象。 以下是使用的示例 `req=props` 要在JavaScript中获取响应图像大小，请执行以下操作™

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
