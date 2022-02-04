---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets,Accessibility
role: Developer,User
exl-id: f0cde820-237c-4594-8a16-d272af4c976b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性。 您可以使用 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性会从按钮的本地化符号的值填充。 禁用按钮时， `aria-disabled` 属性会相应地进行设置。

主视图具有角色 `application`. 有关主视图的简要说明，请参阅 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，则使用提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产在UserData字段中定义了标签，则 `aria-label` 属性的值。
