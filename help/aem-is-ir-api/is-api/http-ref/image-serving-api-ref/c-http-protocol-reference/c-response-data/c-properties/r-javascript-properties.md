---
title: JavaScript资产
description: 如果将JavaScript指定为响应格式，则会对回复数据进行格式化，以便将其解析为JavaScript&trade； include文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: 'https://experienceleague.adobe.com/T6xqUHtT9XX4b9bP-wi-b0dDBe2LHE3vcBcJI6cMKqE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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
