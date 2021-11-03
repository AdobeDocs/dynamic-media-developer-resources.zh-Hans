---
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性。 您可以使用 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性会从按钮的本地化符号的值填充。 禁用按钮时， `aria-disabled` 属性会相应地进行设置。

滑块组件具有角色 `slider` 使用属性 `aria-valuenow`, `aria-valuemin`和 `aria-valuemax` 以描述当前滑块位置。

下拉列表由包含其他 `aria-haspopup` 属性设置为 `true` 和 `aria-controls` 引用实际下拉面板元素的属性。 下拉面板本身具有角色 `menu` 具有角色的子元素 `menuitem`. 每个菜单项都具有 `aria-label` 属性。

模式对话框具有角色 `dialog`. 对话框的标题元素被 `aria-labelledby` 属性。
