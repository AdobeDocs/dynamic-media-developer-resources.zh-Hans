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

顶级查看器元素具有角色 `region` 和 `aria-label` 属性默认设置为查看器的名称。 您可以使用以下内容控制标签 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性填充自按钮本地化符号的值。 当按钮被禁用时， `aria-disabled` 属性会进行相应的设置。

允许您在轮播幻灯片中导航的按钮具有标签，这些标签会根据当前选定的幻灯片在运行时更新。 这些按钮标签的模板设置方式 `CAROUSELVIEWER_TOOLTIP_GOTO` 本地化符号。

主视图具有角色 `application`. 中提供了主视图的简要说明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，用法提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产的UserData字段中定义了标签，则 `aria-label` 属性被设置为此类标签的值。

热点、区域和图像映射将发挥作用 `button` 和描述性文本集 `aria-label` 属性，其值为热点或图像映射标签。 当用户重点关注热点或图像映射时，可以使用为键盘用户提供导航提示 `aria-describedby`，使用提示的文本来自 `USAGE_HINT` 本地化符号。
