---
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频，辅助功能
role: Developer,Business Practitioner
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和具有`aria-label`属性的描述性文本集。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，会相应地设置`aria-disabled`属性。

滑块组件具有角色`slider`（具有属性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`），用于描述当前滑块位置。

缩略图的角色为`dialog`，其属性由`ThumbnailGridView.LABEL`本地化符号控制。 `aria-label`单个缩略图具有`button`角色。 如果选择缩略图，则会将`aria-selected`属性设置为`true`。

显示色板的组件具有角色`listbox`，且`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 单个色板具有角色`option`（具有`aria-setsize`和`aria-posinset`属性），用于描述色板在集中的位置。 如果选择了色板，则将`aria-selected`属性设置为`true`。

下拉列表由按钮激活，其中附加的`aria-haspopup`属性设置为`true`和`aria-controls`属性引用实际的下拉面板元素。 下拉面板本身具有角色`menu`，其子元素具有角色`menuitem`。 每个菜单项都指定了`aria-label`属性。

模式对话框具有`dialog`角色。 该对话框的标题元素被`aria-labelledby`属性引用。
