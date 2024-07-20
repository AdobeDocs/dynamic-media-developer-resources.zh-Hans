---
description: 如果将xml指定为响应格式，则回复数据将格式化为可由任何标准XML解析器解析的XML文档。
solution: Experience Manager
title: XML属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
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
