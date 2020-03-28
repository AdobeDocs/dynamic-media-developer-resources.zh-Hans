---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 52f5dad9-7309-4385-99bc-79d02d3ba2d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

按钮具有角色和 `button` 带属性的描述性文本 `aria-label` 设置。 属性的 `aria-label` 值由按钮的本地化符号的值填充。 当按钮被禁用时，属性 `aria-disabled` 会相应地设置。

滑块组件具有 `slider` 属性和 `aria-valuenow`描述当 `aria-valuemin`前滑块 `aria-valuemax` 位置的角色。

下拉列表由按钮激活，其他属性设 `aria-haspopup` 置为并引用 `true` 实 `aria-controls` 际的下拉面板元素的属性。 下拉面板本身具有子元素 `menu` 具有角色的角色 `menuitem`。 每个菜单项都指定 `aria-label` 了属性。

Modal对话框具有角色 `dialog`。 该对话框的标题元素由属性引 `aria-labelledby` 用。
