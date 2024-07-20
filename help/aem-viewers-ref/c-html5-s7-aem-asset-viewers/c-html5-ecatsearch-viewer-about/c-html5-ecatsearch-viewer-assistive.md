---
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮本地化符号的值填充。 禁用某个按钮后，将相应地设置`aria-disabled`属性。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简短说明，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此类标签的值设置`aria-label`属性。

热点、区域和图像映射具有角色`button`和使用`aria-label`属性设置的描述性文本，并具有热点或图像映射标签的值。 当用户关注热点或图像映射时，使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。

缩略图具有角色`dialog`，该角色的`aria-label`属性由`ThumbnailGridView.LABEL`本地化符号控制。 单个缩略图具有角色`button`。 如果选择了缩略图，则会将`aria-selected`属性设置为`true`。

显示样本的组件具有角色`listbox`，`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 单个样本具有角色`option`，该角色具有`aria-setsize`和`aria-posinset`属性，用于描述样本在集中的位置。 如果选择了样本，它将获得`aria-selected`属性设置为`true`。

下拉列表由按钮激活，这些按钮具有设置为`true`的额外`aria-haspopup`属性和引用实际下拉面板元素的`aria-controls`属性。 下拉面板本身的角色为`menu`，子元素的角色为`menuitem`。 每个菜单项都指定了`aria-label`属性。

搜索用户界面已分组到角色为`search`的元素中。 搜索输入字段具有角色`searchbox`，并引用了由`SearchPanel.INFO_PROMPT`本地化符号控制且具有`aria-describedby`属性的信息标签。

模式对话框具有角色`dialog`。 对话框的标头元素由`aria-labelledby`属性引用。
