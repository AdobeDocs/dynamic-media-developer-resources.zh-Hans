---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮本地化符号的值填充。 禁用某个按钮时，将相应地设置`aria-disabled`属性。

滑块组件的角色`slider`具有属性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`，用于描述当前滑块位置。

下拉列表由按钮激活，这些按钮具有设置为`aria-haspopup`的其他`true`属性和引用实际下拉面板元素的`aria-controls`属性。 下拉面板本身的角色为`menu`，子元素的角色为`menuitem`。 每个菜单项都指定了`aria-label`属性。

模式对话框具有角色`dialog`。 对话框的标头元素由`aria-labelledby`属性引用。
