---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅，辅助功能
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和设置了`aria-label`属性的描述性文本。 `aria-label`属性的值由按钮的本地化符号的值填充。 禁用按钮时，会相应地设置`aria-disabled`属性。

用于在旋转式幻灯片中导航的按钮具有可在运行时更新的标签，具体取决于当前选定的幻灯片。 这些按钮标签的模板使用`CAROUSELVIEWER_TOOLTIP_GOTO`本地化符号设置。

主视图具有角色`application`。 在`aria-roledescription`中提供了主视图的简短描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此标签的值设置`aria-label`属性。

热点、区域和图像映射具有角色`button`和具有`aria-label`属性且具有热点或图像映射标签值的描述性文本集。 当用户将焦点放在热点或图像映射上时，使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。
