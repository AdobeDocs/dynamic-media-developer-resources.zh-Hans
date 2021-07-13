---
description: 交互式图像查看器显示的某些内容需要本地化。 这包括用户界面元素工具提示以及加载时弹出缩放视图显示的信息消息。
title: 用户界面元素的本地化
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 用户界面元素的本地化{#localization-of-user-interface-elements}

交互式图像查看器显示的某些内容需要本地化。 这包括用户界面元素工具提示以及加载时弹出缩放视图显示的信息消息。

查看器中每个可以本地化的文本内容都由名为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有随现成查看器提供的英语区域设置(`"en"`)的默认关联文本值，并且还可以根据需要为任意数量的区域设置设置用户定义的值。

查看器启动时，它会检查当前区域设置，以查看此区域设置的每个支持的SYMBOL是否有用户定义的值。 如果存在，则使用用户定义的值；否则，它会回退到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递到查看器。 此类对象包含支持的区域设置列表、每个区域设置的SYMBOL文本值以及默认区域设置。

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

在上例中，本地化对象定义了两个区域设置（`"en"`和`"fr"`），并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应该将本地化对象作为配置对象的`localizedTexts`字段的值传递给查看器构造函数。 替代选项是通过调用`setLocalizedTexts(localizationInfo)`方法来传递本地化对象。

支持以下符号：

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
