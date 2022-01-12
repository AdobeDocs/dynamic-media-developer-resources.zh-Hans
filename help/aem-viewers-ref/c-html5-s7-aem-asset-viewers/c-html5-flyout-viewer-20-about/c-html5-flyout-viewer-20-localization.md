---
title: 用户界面元素的本地化
description: 弹出查看器显示的某些内容需要本地化。 此内容包括用户界面元素工具提示和信息消息，这些消息在加载时通过弹出缩放视图显示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 57941e90-1462-43e6-80db-6b111e004f9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 用户界面元素的本地化{#localization-of-user-interface-elements}

弹出查看器显示的某些内容需要本地化。 此内容包括用户界面元素工具提示和信息消息，这些消息在加载时通过弹出缩放视图显示。

查看器中每个可以本地化的文本内容都由一个名为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有英语区域设置( `"en"`)。 它还可以根据需要为所需数量的区域设置用户定义的值。

查看器启动时，它会检查当前区域设置，以查看区域设置的每个支持的SYMBOL是否有用户定义的值。 如果存在，则使用用户定义的值；否则，它会回退到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递到查看器。 此类对象包含支持的区域设置列表、每个区域设置的SYMBOL文本值以及默认区域设置。

此类本地化对象的示例如下：

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

在上例中，本地化对象定义了两个区域设置( `"en"` 和 `"fr"`)，并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应将本地化对象作为的值传递给查看器构造函数 `localizedTexts` 配置对象的字段。 替代选项是通过调用 `setLocalizedTexts(localizationInfo)` 方法。

支持以下符号：

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>符号 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 容器.LABEL </span> </p> </td> 
   <td colname="col2"> <p>顶级查看器元素的ARIA标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>主视图组件的ARIA角色描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>键盘用户的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>桌面系统的信息消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>触控设备的信息消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>滚动左键的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>滚动右键的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>“向上滚动”按钮的工具提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>向下滚动按钮的工具提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
