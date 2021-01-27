---
description: 电子目录查看器显示的某些内容受本地化的约束，包括缩放按钮、页面更改按钮、缩略图按钮、全屏按钮、关闭按钮和滚动条按钮。
seo-description: 电子目录查看器显示的某些内容受本地化的约束，包括缩放按钮、页面更改按钮、缩略图按钮、全屏按钮、关闭按钮和滚动条按钮。
seo-title: 本地化用户界面元素
solution: Experience Manager
title: 本地化用户界面元素
topic: Dynamic Media
uuid: bd95c7dc-3158-4cca-81d4-f5efd57c0124
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 0%

---


# 用户界面元素本地化{#localization-of-user-interface-elements}

电子目录查看器显示的某些内容受本地化的约束，包括缩放按钮、页面更改按钮、缩略图按钮、全屏按钮、关闭按钮和滚动条按钮。

查看器中每个可本地化的文本内容都由一个称为SYMBOL的特殊查看器SDK标识符来表示。 任何SYMBOL都具有随现成查看器提供的英语区域设置(`"en"`)的默认关联文本值，并且可能还根据需要为任意多个区域设置设置用户定义的值。

查看器开始时，它检查当前区域设置，以查看区域设置中每个支持的SYMBOL是否有用户定义的值。 如果存在，则使用用户定义的值；否则，它将返回现成的默认文本。

用户定义的本地化数据可作为本地化JSON对象传递到查看器。 这样的对象包含支持的语言环境列表、每个语言环境的SYMBOL文本值以及默认语言环境。

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

在上面的示例中，本地化对象定义两个区域设置（`"en"`和`"fr"`），并为每个区域设置中的两个用户界面元素提供本地化。

网页代码应将此类本地化对象作为配置对象的`localizedTexts`字段的值传递给查看器构造函数。 替代选项是通过调用`setLocalizedTexts(localizationInfo)`方法传递本地化对象。

支持以下SYMBOL(假定containerId是查看器容器的ID):

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
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>主视图组件的ARIA角色描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>键盘用户的ARIA使用提示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>放大按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>缩小按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>缩放重置按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>全屏按钮处于正常状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“全屏”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>向上滚动按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>向下滚动按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_rightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>大的下一页按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_leftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>“大上一页”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_lastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>“最后一页”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>“最后一页”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_firstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>首页按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>首页按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarRightButton.PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>下一页按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>“上一页”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>缩览图模式下的缩览图按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>缩览图按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>“信息面板”关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>社交共享工具。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>电子邮件共享按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>电子邮件对话框标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>“电子邮件”对话框右上角关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESS  </span> </p> </td> 
   <td colname="col2"> <p>电子邮件地址格式错误时显示的错误消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO  </span> </p> </td> 
   <td colname="col2"> <p>“至”输入字段的标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD  </span> </p> </td> 
   <td colname="col2"> <p>添加其他电子邮件地址按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD  </span> </p> </td> 
   <td colname="col2"> <p>添加其他电子邮件地址按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM  </span> </p> </td> 
   <td colname="col2"> <p>从输入字段。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE  </span> </p> </td> 
   <td colname="col2"> <p>消息输入字段。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE  </span> </p> </td> 
   <td colname="col2"> <p>“删除电子邮件地址”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>“全选”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>选择“全部”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>表单提交后对话框底部显示的关闭按钮的说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>提交表单后对话框底部显示的“关闭”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>表单提交按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>表单提交按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS  </span> </p> </td> 
   <td colname="col2"> <p>成功发送电子邮件时显示确认消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE  </span> </p> </td> 
   <td colname="col2"> <p>电子邮件未成功发送时显示的错误消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>嵌入共享按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>嵌入对话框标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>嵌入对话框右上关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>嵌入代码文本的说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>嵌入大小组合框的标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>嵌入大小组合框中最后一个“自定义大小”条目的文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>链接共享按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>链接对话框标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>“链接”对话框右上角关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>共享链接的说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>“全选”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> 选择“全部”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Facebook共享按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Twitter共享按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>打印按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>打印对话框标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>打印对话框右上关闭按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE  </span> </p> </td> 
   <td colname="col2"> <p>“选择打印页面”部分的标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT  </span> </p> </td> 
   <td colname="col2"> <p>“当前页面”单选按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM  </span> </p> </td> 
   <td colname="col2"> <p>“跨页范围自”单选按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO  </span> </p> </td> 
   <td colname="col2"> <p>“to”数字选取器的标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL  </span> </p> </td> 
   <td colname="col2"> <p>“所有页面”单选按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PRINT.PAGE_HANDLING  </span> </p> </td> 
   <td colname="col2"> <p>“页面处理”部分的标签。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE  </span> </p> </td> 
   <td colname="col2"> <p>“每页1页”单选按钮的标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO  </span> </p> </td> 
   <td colname="col2"> <p>“每张2页”单选按钮的标题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 打印。CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>“取消”按钮的描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p> “取消”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>“发送到打印”按钮的描述 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> “发送至打印”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 收藏夹菜单。工具提示  </span> </p> </td> 
   <td colname="col2"> <p>收藏夹菜单按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“添加收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“添加收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>编辑收藏夹模式下的“删除收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“删除收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“视图所有收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>“视图所有收藏夹”按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 收藏夹效果。工具提示  </span> </p> </td> 
   <td colname="col2"> <p>单个收藏夹图标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY]  </span> </p> </td> 
   <td colname="col2"> <p>查看器在加载时生成的页面标签。 </p> <p>该符号的名称是模板，其中<span class="codeph"> XX </span>是横向从零开始的跨页索引，可选<span class="codeph"> YY </span>是<span class="codeph"> XX </span>所定位跨页中从零开始的页索引。 </p> <p>仅适用于初始加载的资产；如果使用<span class="codeph"> setAsset()</span> API调用更改了资产，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM  </span> </p> </td> 
   <td colname="col2"> <p> 在跨页中为左页和右页定义标签时，用作页面标签分隔符的字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>主控制栏向左滚动按钮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>主控件条向右滚动按钮。 </p> </td> 
  </tr> 
 </tbody> 
</table>

