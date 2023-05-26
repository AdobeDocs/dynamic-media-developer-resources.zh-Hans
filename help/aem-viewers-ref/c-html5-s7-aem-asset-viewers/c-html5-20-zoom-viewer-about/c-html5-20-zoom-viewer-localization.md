---
title: 用户界面元素的本地化
description: Video Viewer显示的某些内容必须进行本地化，包括缩放按钮和全屏按钮。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 用户界面元素的本地化{#localization-of-user-interface-elements}

Video Viewer显示的某些内容必须进行本地化，包括缩放按钮和全屏按钮。

查看器中所有可以本地化的文本内容都由一个名为SYMBOL的特殊Viewer SDK标识符表示。 任何SYMBOL都有英语区域设置( `"en"`)。 此外，还可以根据需要为任意数量的区域设置用户定义的值。

当查看器启动时，它会检查当前区域设置，查看区域设置的每个受支持的SYMBOL是否存在用户定义的值。 如果存在，则使用用户定义的值；否则，它会返回到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递给查看器。 此类对象包含支持的区域设置列表、每个区域设置的SYMBOL文本值和默认区域设置。

以下是此类本地化对象的示例：

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

在上例中，本地化对象定义了两个区域设置( `"en"` 和 `"fr"`)并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应将此类本地化对象作为的值传递给查看器构造函数 `localizedTexts` 配置对象的字段。 替代选项是通过调用 `setLocalizedTexts(localizationInfo)` 方法。

支持以下SYMBOL：

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符号 </p> </th> 
   <th colname="col2" class="entry"> <p>的工具提示…… </p> </th> 
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
   <td colname="col2"> <p>全屏按钮处于正常状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECT </span> </p> </td> 
   <td colname="col2"> <p>全屏按钮处于全屏状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>“向左滚动”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向右滚动按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向上滚动按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向下滚动按钮。 </p> </td> 
  </tr> 
 </tbody> 
</table>
