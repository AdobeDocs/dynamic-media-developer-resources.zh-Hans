---
title: 用户界面元素的本地化
description: 轮播查看器显示的某些内容需要进行本地化。 此内容包括幻灯片导航按钮。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 用户界面元素的本地化{#localization-of-user-interface-elements}

轮播查看器显示的某些内容需要进行本地化。 此内容包括幻灯片导航按钮。

查看器中的每个可本地化的文本内容都由名为SYMBOL的特殊查看器SDK标识符表示。 任何SYMBOL都具有随开箱即用查看器提供的英语区域设置(`"en"`)的默认关联文本值，并且还可以根据需要为多个区域设置设置用户定义的值。

当查看器启动时，它会检查当前区域设置，查看此类区域设置的每个受支持的SYMBOL是否存在用户定义的值。 如果存在，则使用用户定义的值；否则，它会回退到现成的默认文本。

用户定义的本地化数据可以作为本地化JSON对象传递给查看器。 此类对象包含支持的区域设置列表、每个区域设置的SYMBOL文本值以及默认区域设置。

以下是此类本地化对象的示例：

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>已选择播放暂停按钮状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>未选择的播放暂停按钮状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELEVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> 上一张幻灯片按钮和下一张幻灯片按钮的工具提示和ARIA标签。 </p> <p>接受两个替换令牌：当前幻灯片索引为<span class="codeph"> $CURRENT_FRAME$ </span>，幻灯片总数为<span class="codeph"> $TOTAL_FRAMES$ </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> 顶级查看器元素的ARIA标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> 主视图组件的ARIA角色描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> 键盘用户的ARIA使用提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
