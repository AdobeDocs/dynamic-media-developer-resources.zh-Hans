---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索，辅助功能
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，将相应设置`aria-disabled`属性。

主视图具有角色`application`。 在`aria-roledescription`中提供了主视图的简短描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此标签的值设置`aria-label`属性。

热点、区域和图像映射具有角色`button`和具有`aria-label`属性且具有热点或图像映射标签值的描述性文本集。 当用户将焦点放在热点或图像映射上时，使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。

缩览图具有由`ThumbnailGridView.LABEL`本地化符号控制的`aria-label`属性的角色`dialog`。 各个缩略图具有角色`button`。 如果选择了缩略图，则会将`aria-selected`属性设置为`true`。

显示色板的组件具有角色`listbox`，其`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 各个色板具有`aria-setsize`和`aria-posinset`属性的角色`option`，用于描述色板在集中的位置。 如果选择了色板，则获取设置为`true`的`aria-selected`属性。

下拉列表由按钮激活，附加`aria-haspopup`属性设置为`true`，而`aria-controls`属性引用实际的下拉面板元素。 下拉面板本身具有角色`menu`，子元素具有角色`menuitem`。 每个菜单项都指定了`aria-label`属性。

搜索用户界面将分组在角色为`search`的元素中。 搜索输入字段具有角色`searchbox`，并引用由`SearchPanel.INFO_PROMPT`本地化符号控制且属性为`aria-describedby`的信息标签。

Modal对话框具有角色`dialog`。 对话框的标头元素由`aria-labelledby`属性引用。
