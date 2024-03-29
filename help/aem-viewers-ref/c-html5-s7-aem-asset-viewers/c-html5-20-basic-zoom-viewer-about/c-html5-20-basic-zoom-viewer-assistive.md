---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性默认设置为查看器的名称。 您可以使用以下内容控制标签 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本设置 `aria-label` 属性。 的值 `aria-label` 属性填充自按钮本地化符号的值。 禁用某个按钮后， `aria-disabled` 属性会进行相应的设置。

主视图具有角色 `application`. 中提供了主视图的简要说明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，用法提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产的UserData字段中定义了标签，则 `aria-label` 属性被设置为此类标签的值。
