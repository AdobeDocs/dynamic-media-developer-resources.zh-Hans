---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频，辅助功能
role: 开发人员，商业从业者
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和设置了`aria-label`属性的描述性文本。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，会相应地设置`aria-disabled`属性。

滑块组件具有`slider`角色，其属性为`aria-valuenow`、`aria-valuemin`和`aria-valuemax`以描述当前滑块位置。

缩览图具有由`ThumbnailGridView.LABEL`本地化符号控制的`aria-label`属性的角色`dialog`。 各个缩略图具有角色`button`。 如果选择了缩略图，则会将`aria-selected`属性设置为`true`。

显示色板的组件具有角色`listbox`，其`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 各个色板具有`aria-setsize`和`aria-posinset`属性的角色`option`，用于描述色板在集中的位置。 如果选择了色板，则获取设置为`true`的`aria-selected`属性。

下拉列表由按钮激活，附加`aria-haspopup`属性设置为`true`,`aria-controls`属性引用实际的下拉面板元素。 下拉面板本身具有角色`menu`，子元素具有角色`menuitem`。 每个菜单项都指定了`aria-label`属性。

Modal对话框具有角色`dialog`。 对话框的标头元素由`aria-labelledby`属性引用。
