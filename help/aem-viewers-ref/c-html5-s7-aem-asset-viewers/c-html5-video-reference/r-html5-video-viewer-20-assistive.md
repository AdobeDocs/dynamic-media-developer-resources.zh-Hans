---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic Media
uuid: e7090fb1-9458-4f97-a11f-5b0600a13db0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，将相应设置`aria-disabled`属性。

滑块组件具有`aria-valuenow`、`aria-valuemin`和`aria-valuemax`属性的角色`slider`，用于描述当前滑块位置。

下拉列表由附加的`aria-haspopup`属性设置为`true`和`aria-controls`属性并引用实际的下拉面板元素的按钮来激活。 下拉面板本身具有角色`menu`，子元素具有角色`menuitem`。 每个菜单项都指定了`aria-label`属性。

Modal对话框具有角色`dialog`。 对话框的标题元素由`aria-labelledby`属性引用。
