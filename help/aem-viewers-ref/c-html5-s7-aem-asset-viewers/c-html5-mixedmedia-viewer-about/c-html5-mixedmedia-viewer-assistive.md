---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets,Accessibility
role: Developer,User
exl-id: 6cf7f739-cbfb-4fac-8632-904a0d40ad05
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性默认设置为查看器的名称。 您可以使用以下内容控制标签 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性填充自按钮本地化符号的值。 当按钮被禁用时， `aria-disabled` 属性会进行相应的设置。

主视图具有角色 `application`. 中提供了主视图的简要说明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，用法提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产的UserData字段中定义了标签，则 `aria-label` 属性被设置为此类标签的值。

显示样本的组件具有此角色 `listbox` 替换为 `aria-label` 属性设置为的值 `LABEL` 该组件的本地化符号。 单个样本具有此角色 `option` 替换为 `aria-setsize` 和 `aria-posinset` 属性，用于描述样本集内的样本位置。 如果选择了样本，它将获得 `aria-selected` 属性设置为 `true`.

滑块组件具有此角色 `slider` 具有属性 `aria-valuenow`， `aria-valuemin`、和 `aria-valuemax` 以描述当前滑块位置。
