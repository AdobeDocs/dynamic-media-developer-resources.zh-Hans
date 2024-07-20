---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简短说明，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此类标签的值设置`aria-label`属性。

显示样本的组件具有角色`listbox`，`aria-label`属性设置为该组件的`LABEL`本地化符号的值。 单个样本具有角色`option`，该角色具有`aria-setsize`和`aria-posinset`属性，用于描述样本在集中的位置。 如果选择了样本，它将获得`aria-selected`属性设置为`true`。
