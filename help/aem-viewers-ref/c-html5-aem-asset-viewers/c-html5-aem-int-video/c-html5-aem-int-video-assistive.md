---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

按钮具有角色和 `button` 带属性的描述性文本 `aria-label` 设置。 属性的 `aria-label` 值由按钮的本地化符号的值填充。 当按钮被禁用时，属性 `aria-disabled` 会相应地设置。

滑块组件具有 `slider` 属性和 `aria-valuenow`描述当 `aria-valuemin`前滑块 `aria-valuemax` 位置的角色。

缩览图具有由 `dialog` 本地化 `aria-label` 符号控制的属性 `ThumbnailGridView.LABEL` 角色。 单个缩略图具有角色 `button`。 如果选择了缩略图，则会将其 `aria-selected` 属性设置为 `true`。

显示色板的组件具有将属 `listbox` 性设 `aria-label` 置为该组件本地化符号值的 `LABEL` 角色。 各个色板具有用于描 `option` 述集 `aria-setsize` 中的色 `aria-posinset` 板位置的具有和属性的角色。 如果选择了色板，则其属性 `aria-selected` 将设置为 `true`。

下拉列表由按钮激活，其他属性设 `aria-haspopup` 置为并引用 `true` 实 `aria-controls` 际的下拉面板元素的属性。 下拉面板本身具有子元素 `menu` 具有角色的角色 `menuitem`。 每个菜单项都指定 `aria-label` 了属性。

Modal对话框具有角色 `dialog`。 该对话框的标题元素由属性引 `aria-labelledby` 用。
