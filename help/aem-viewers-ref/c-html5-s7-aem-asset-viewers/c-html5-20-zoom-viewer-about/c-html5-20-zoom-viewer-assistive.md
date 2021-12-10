---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性。 您可以使用 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性会从按钮的本地化符号的值填充。 禁用按钮时， `aria-disabled` 属性会相应地进行设置。

主视图具有角色 `application`. 有关主视图的简要说明，请参阅 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，则使用提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产在UserData字段中定义了标签，则 `aria-label` 属性的值。

显示色板的组件具有角色 `listbox` with `aria-label` 属性设置为 `LABEL` 该组件的本地化符号。 单个色板具有 `option` with `aria-setsize` 和 `aria-posinset` 属性来描述集中的色板位置。 如果选择了色板，则会获得 `aria-selected` 属性设置为 `true`.
