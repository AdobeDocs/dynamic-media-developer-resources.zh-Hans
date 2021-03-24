---
description: 如果将JavaScript™指定为响应格式，则返回数据的格式将被分析为JavaScript™包含文件。
solution: Experience Manager
title: JavaScript™属性
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# JavaScript™属性{#javascript-properties}

如果将JavaScript™指定为响应格式，则返回数据的格式将被分析为JavaScript™包含文件。

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

*`propertyValue`* 可以是空的。在每行的开头和结尾以及=分隔符前后，空格是可选的。 所有值都用单引号括起来。 字符串中的单引号用两个连续的单引号进行转义。

要分析JavaScript™属性响应，必须在加载属性文件之前创建响应中引用的任何对象或对象。 以下是使用`req=props`在JavaScript™中获得响应图像大小的示例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

