---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮本地化符号的值填充。 禁用某个按钮时，将相应地设置`aria-disabled`属性。

允许您在轮播幻灯片中导航的按钮具有标签，这些标签会根据当前选定的幻灯片在运行时更新。 这些按钮标签的模板设置了`CAROUSELVIEWER_TOOLTIP_GOTO`本地化符号。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简短说明，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此类标签的值设置`aria-label`属性。

热点、区域和图像映射具有角色`button`和使用`aria-label`属性设置的描述性文本，并具有热点或图像映射标签的值。 当用户关注热点或图像映射时，使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。
