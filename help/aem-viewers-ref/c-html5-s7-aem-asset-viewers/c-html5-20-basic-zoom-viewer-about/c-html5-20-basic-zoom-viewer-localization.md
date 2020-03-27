---
description: 基本缩放查看器显示的某些内容受本地化的约束，包括缩放按钮和全屏按钮。
seo-description: 基本缩放查看器显示的某些内容受本地化的约束，包括缩放按钮和全屏按钮。
seo-title: 本地化用户界面元素
solution: Experience Manager
title: 本地化用户界面元素
topic: Dynamic media
uuid: 842970d9-0882-4163-8c49-3ea35d372d35
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 本地化用户界面元素{#localization-of-user-interface-elements}

基本缩放查看器显示的某些内容受本地化的约束，包括缩放按钮和全屏按钮。

查看器中每个可本地化的文本内容都由称为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有随现成查看器提供的英语区域设置( `"en"`)的默认关联文本值，并且可能还为所需数量的区域设置用户定义的值。

查看器开始时，它检查当前区域设置，以查看区域设置中每个支持的SYMBOL是否有用户定义的值。 如果存在，则使用用户定义的值；否则，它会回落到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递给查看器。 这样的对象包含支持的区域设置的列表、每个区域设置的SYMBOL文本值以及默认区域设置。

此类本地化对象的示例：

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

在上面的示例中，本地化对象定义了两个区域设置( `"en"` 和 `"fr"`)，并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应将此类本地化对象作为配置对象字段的值传递给查 `localizedTexts` 看器构造函数。 替代选项是通过调用方法传递本地化对 `setLocalizedTexts(localizationInfo)` 象。

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
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL </span> </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>放大按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>缩小按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>缩放重置按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>全屏按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>全屏状态的全屏按钮。 </p> </td> 
  </tr> 
 </tbody> 
</table>

