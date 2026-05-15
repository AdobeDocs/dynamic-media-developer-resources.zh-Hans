---
title: 用户界面元素的本地化
description: 交互式图像查看器显示的某些内容需要进行本地化。 此内容包括用户界面元素工具提示和加载时弹出缩放视图显示的信息消息。
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
autotag-review: '2026-05-13T22:17:15.458Z'
TQID: 'https://experienceleague.adobe.com/XYvxUsA4fiBhf5gT35bxHZTo9Tn6QvT5ld89zNnHiOo'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 0%

---

# 用户界面元素的本地化{#localization-of-user-interface-elements}

交互式图像查看器显示的某些内容需要进行本地化。 此内容包括用户界面元素工具提示和加载时弹出缩放视图显示的信息消息。

查看器中可本地化的每个文本内容都由名为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有随开箱即用查看器提供的英语区域设置(`"en"`)的缺省关联文本值，并且可以根据需要为任意多个区域设置设置用户定义的值。

当查看器启动时，它会检查当前区域设置，查看此类区域设置的每个受支持的SYMBOL是否存在用户定义的值。 如果存在，则使用用户定义的值；否则，它会回退到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递给查看器。 此类对象包含支持的区域设置列表、每个区域设置的SYMBOL文本值以及默认区域设置。

以下是此类本地化对象的示例：

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

在上述示例中，本地化对象定义了两个区域设置（`"en"`和`"fr"`），并为每个区域设置中的两个用户界面元素提供了本地化。

网页代码应将本地化对象作为配置对象的`localizedTexts`字段的值传递给查看器构造函数。 另一种选择是通过调用`setLocalizedTexts(localizationInfo)`方法来传递本地化对象。

支持以下SYMBOL：

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符号 </p> </th> 
   <th colname="col2" class="entry"> <p>工具提示…… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>顶级查看器元素的ARIA标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主视图组件的ARIA角色描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>键盘用户的ARIA使用提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
