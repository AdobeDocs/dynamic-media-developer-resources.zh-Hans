---
description: 如果将xml指定为响应格式，则回复数据将格式化为可由任何标准XML解析器解析的XML文档。
solution: Experience Manager
title: XML属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# XML属性{#xml-properties}

如果将xml指定为响应格式，则回复数据将格式化为可由任何标准XML解析器解析的XML文档。

典型的属性响应文档具有以下一般结构：

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

`<prop-group>`元素用作最外部的容器，并用于分组属性。 如果某个组被命名为，则该名称将对应于Java/JavaScript对象名称。

>[!NOTE]
>
>可以为某些`req=`类型指定字符编码。 有关详细信息，请参阅特定`req=`命令的描述。
