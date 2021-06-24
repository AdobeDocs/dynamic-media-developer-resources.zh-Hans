---
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放，辅助功能
role: Developer,Business Practitioner
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下，该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简要描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则`aria-label`属性将使用此标签的值进行设置。

显示色板的组件具有角色`listbox`，且`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 单个色板具有角色`option`（具有`aria-setsize`和`aria-posinset`属性），用于描述色板在集中的位置。 如果选择了色板，则将`aria-selected`属性设置为`true`。
