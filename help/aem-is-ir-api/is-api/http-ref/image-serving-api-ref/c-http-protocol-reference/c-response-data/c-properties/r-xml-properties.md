---
description: 如果将xml指定为响应格式，则返回数据将格式化为XML文档，任何标准XML分析器都可以分析该格式。
solution: Experience Manager
title: XML属性
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# XML属性{#xml-properties}

如果将xml指定为响应格式，则返回数据将格式化为XML文档，任何标准XML分析器都可以分析该格式。

典型属性响应文档具有以下通用结构：

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

`<prop-group>`元素用作最外面的容器和分组属性。 如果组被命名，则该名称与Java/JavaScript对象名称相对应。

>[!NOTE]
>
>可以为某些`req=`类型指定字符编码。 有关详细信息，请参阅特定`req=`命令的说明。

