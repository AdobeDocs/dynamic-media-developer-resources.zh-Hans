---
description: 如果将JavaScript™指定为响应格式，则将格式化回复数据，以将其解析为JavaScript™包含文件。
solution: Experience Manager
title: JavaScript™属性
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# JavaScript™属性{#javascript-properties}

如果将JavaScript™指定为响应格式，则将格式化回复数据，以将其解析为JavaScript™包含文件。

典型的JavaScript™属性响应具有以下通用结构：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可为空。在每行的开头和结尾以及=分隔符前后的空格都是可选的。 所有值都用单引号括起来。 字符串中的单引号会使用两个连续的单引号进行转义。

要解析JavaScript™属性响应，必须在加载属性文件之前创建响应中引用的任何对象或对象。 以下示例用于在JavaScript™中使用`req=props`获取响应图像大小：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
