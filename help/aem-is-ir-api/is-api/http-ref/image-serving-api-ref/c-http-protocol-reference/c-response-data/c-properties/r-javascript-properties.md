---
description: 如果将javascript指定为响应格式，则将返回数据格式化为JavaScript包含文件。
seo-description: 如果将javascript指定为响应格式，则将返回数据格式化为JavaScript包含文件。
seo-title: JavaScript属性
solution: Experience Manager
title: JavaScript属性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScript属性{#javascript-properties}

如果将javascript指定为响应格式，则将返回数据格式化为JavaScript包含文件。

典型的JavaScript属性响应具有以下通用结构：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可能是空的。在每行的开始和结尾以及=分隔符前后，空白是可选的。 所有值都用单引号括起来。 字符串中的单引号使用两个连续的单引号进行转义。

要分析JavaScript属性响应，必须在加载属性文件之前创建响应中引用的任何对象。 以下是使用`req=props`在JavaScript中获得响应图像大小的示例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

