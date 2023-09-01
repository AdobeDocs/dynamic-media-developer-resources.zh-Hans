---
title: JavaScript属性
description: 如果将JavaScript指定为响应格式，则会将回复数据格式化，以便将其解析为JavaScript&trade；包含文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# JavaScript属性{#javascript-properties}

如果将JavaScript指定为响应格式，则会将回复数据格式化，以便将其解析为JavaScript包含文件。

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

此 *`propertyValue`* 可以为空。 在每行的开始和结束位置以及=分隔符之前和之后，空格是可选的。 所有值都用单引号括起来。 字符串中的单引号使用两个连续的单引号进行转义。

要分析JavaScript属性响应，必须在加载属性文件之前创建响应中引用的任何对象。 以下是使用的示例 `req=props` 要在JavaScript中获取响应图像大小，请执行以下操作：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
