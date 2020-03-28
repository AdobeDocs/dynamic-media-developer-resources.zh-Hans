---
description: 如果将javascript指定为响应格式，则返回数据的格式将被解析为JavaScript包含文件。
seo-description: 如果将javascript指定为响应格式，则返回数据的格式将被解析为JavaScript包含文件。
seo-title: JavaScript属性
solution: Experience Manager
title: JavaScript属性
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JavaScript属性{#javascript-properties}

如果将javascript指定为响应格式，则返回数据的格式将被解析为JavaScript包含文件。

典型的JavaScript属性响应具有以下常规结构：

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 可能是空的。 在每行的开始和结尾处以及=分隔符前后的空白是可选的。 所有值都用单引号引起来。 字符串中的单引号用两个连续的单引号进行转义。

要解析JavaScript属性响应，必须在加载属性文件之前创建响应中引用的任何对象。 以下是在JavaScript中使用 `req=props` 获取响应图像大小的示例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

