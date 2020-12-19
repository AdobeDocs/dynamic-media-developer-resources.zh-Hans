---
description: 交互式图像查看器显示的某些内容受本地化的约束。 这包括用户界面元素工具提示和加载时由弹出缩放视图显示的信息消息。
seo-description: 交互式图像查看器显示的某些内容受本地化的约束。 这包括用户界面元素工具提示和加载时由弹出缩放视图显示的信息消息。
seo-title: 本地化用户界面元素
title: 本地化用户界面元素
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# 用户界面元素本地化{#localization-of-user-interface-elements}

交互式图像查看器显示的某些内容受本地化的约束。 这包括用户界面元素工具提示和加载时由弹出缩放视图显示的信息消息。

查看器中每个可本地化的文本内容都由称为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有随现成查看器提供的英语区域设置(`"en"`)的默认关联文本值，并且可能还根据需要为任意多个区域设置设置用户定义的值。

查看器开始时，它检查当前区域设置，以查看此类区域设置的每个支持的SYMBOL是否有用户定义的值。 如果存在，则使用用户定义的值；否则，它将返回现成的默认文本。

用户定义的本地化数据可作为本地化JSON对象传递到查看器。 此类对象包含支持的语言环境列表、每个语言环境的SYMBOL文本值以及默认语言环境。

此类本地化对象的示例如下：

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
}, 
defaultLocale:"en" 
}
```

在上面的示例中，本地化对象定义两个区域设置（`"en"`和`"fr"`），并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应将本地化对象作为配置对象的`localizedTexts`字段的值传递给查看器构造函数。 替代选项是通过调用`setLocalizedTexts(localizationInfo)`方法传递本地化对象。

支持以下SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符号 </p> </th> 
   <th colname="col2" class="entry"> <p>工具提示…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>顶级查看器元素的ARIA标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>主视图组件的ARIA角色描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>键盘用户的ARIA使用提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

