---
description: 如果将xml指定为响应格式，则返回数据将格式化为XML文档，XML文档可由任何标准XML解析器解析。
solution: Experience Manager
title: XML属性
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# XML属性{#xml-properties}

如果将xml指定为响应格式，则返回数据将格式化为XML文档，XML文档可由任何标准XML解析器解析。

典型的属性响应文档具有以下通用结构：

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

`<prop-group>`元素用作最外部的容器，并用于分组属性。 如果某个组名为，则该名称对应于Java/JavaScript对象名称。

>[!NOTE]
>
>可以为某些`req=`类型指定字符编码。 有关详细信息，请参阅特定`req=`命令的说明。
