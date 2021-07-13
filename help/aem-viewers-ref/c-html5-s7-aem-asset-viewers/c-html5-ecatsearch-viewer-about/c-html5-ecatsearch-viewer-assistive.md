---
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索，辅助功能
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和具有`aria-label`属性的描述性文本集。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，将相应地设置`aria-disabled`属性。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简要描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则`aria-label`属性将使用此标签的值进行设置。

热点、区域和图像映射具有角色`button`和具有`aria-label`属性的描述性文本集，且具有热点或图像映射标签的值。 当用户将焦点放在热点或图像映射上时，将使用`aria-describedby`为键盘用户提供导航提示，其中使用提示的文本来自`USAGE_HINT`本地化符号。

缩略图的角色为`dialog`，其属性由`ThumbnailGridView.LABEL`本地化符号控制。 `aria-label`单个缩略图具有`button`角色。 如果选择缩略图，则会将`aria-selected`属性设置为`true`。

显示色板的组件具有角色`listbox`，且`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 单个色板具有角色`option`（具有`aria-setsize`和`aria-posinset`属性），用于描述色板在集中的位置。 如果选择了色板，则将`aria-selected`属性设置为`true`。

下拉列表由按钮激活，其中附加的`aria-haspopup`属性设置为`true`，而`aria-controls`属性引用实际的下拉面板元素。 下拉面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每个菜单项都指定了`aria-label`属性。

搜索用户界面将分组到具有`search`角色的元素中。 搜索输入字段具有角色`searchbox`，并引用由`SearchPanel.INFO_PROMPT`本地化符号控制且具有`aria-describedby`属性的信息标签。

模式对话框具有`dialog`角色。 该对话框的标题元素被`aria-labelledby`属性引用。
