---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放，辅助功能
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

主视图具有角色`application`。 在`aria-roledescription`中提供了主视图的简短描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此标签的值设置`aria-label`属性。

显示色板的组件具有角色`listbox`，其`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 各个色板具有`aria-setsize`和`aria-posinset`属性的角色`option`，用于描述色板在集中的位置。 如果选择了色板，则获取设置为`true`的`aria-selected`属性。
