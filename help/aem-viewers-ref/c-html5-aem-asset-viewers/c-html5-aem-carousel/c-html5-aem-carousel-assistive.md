---
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic，查看器，SDK/API，轮播横幅，辅助功能
role: Developer,Business Practitioner
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: f464a7adcb8035a5bdebf1a6c9b647ba04535431
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和具有`aria-label`属性的描述性文本集。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，会相应地设置`aria-disabled`属性。

用于在轮播幻灯片中导航的按钮具有在运行时更新的标签，具体取决于当前选定的幻灯片。 这些按钮标签的模板使用`CAROUSELVIEWER_TOOLTIP_GOTO`本地化符号进行设置。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简要描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则`aria-label`属性将使用此标签的值进行设置。

热点、区域和图像映射具有角色`button`和具有`aria-label`属性的描述性文本集，且具有热点或图像映射标签的值。 当用户将焦点放在热点或图像映射上时，将使用`aria-describedby`为键盘用户提供导航提示，其中使用提示的文本来自`USAGE_HINT`本地化符号。
