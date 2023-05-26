---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性默认设置为查看器的名称。 您可以使用以下内容控制标签 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性填充自按钮本地化符号的值。 当按钮被禁用时， `aria-disabled` 属性会进行相应的设置。

滑块组件具有此角色 `slider` 具有属性 `aria-valuenow`， `aria-valuemin`、和 `aria-valuemax` 以描述当前滑块位置。

下拉列表由具有其他功能的按钮激活 `aria-haspopup` 属性设置为 `true` 和 `aria-controls` 引用实际下拉面板元素的属性。 下拉面板本身具有角色 `menu` 具有子元素角色 `menuitem`. 每个菜单项都具有 `aria-label` 指定的属性。

模式对话框具有角色 `dialog`. 对话框的标头元素由 `aria-labelledby` 属性。
