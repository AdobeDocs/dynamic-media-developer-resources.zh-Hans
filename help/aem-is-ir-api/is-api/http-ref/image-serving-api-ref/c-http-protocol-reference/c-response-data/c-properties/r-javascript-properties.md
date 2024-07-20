---
title: JavaScript资产
description: 如果将JavaScript指定为响应格式，则会对回复数据进行格式化，以便将其解析为JavaScript&amp；trade； include文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# JavaScript资产{#javascript-properties}

如果将JavaScript指定为响应格式，则会对回复数据进行格式化，以便将其解析为JavaScript包含文件。

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

*`propertyValue`*&#x200B;可以为空。 在每行的开始和结束位置以及=分隔符之前和之后，空格是可选的。 所有值都用单引号括起来。 字符串中的单引号使用两个连续的单引号进行转义。

要分析JavaScript属性响应，必须在加载属性文件之前创建响应中引用的任何对象。 以下是使用`req=props`在JavaScript中获取响应图像大小的示例：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
