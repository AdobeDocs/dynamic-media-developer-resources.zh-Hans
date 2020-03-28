---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

主要视图有作用 `application`. 在中提供了主视图的简短描述 `aria-roledescription`，其值由相应主视图组件的 `ROLE_DESCRIPTION` 本地化符号定义。 为键盘用户提供的导航提示 `aria-describedby`使用，使用提示的文本来自本地化 `USAGE_HINT` 符号。 如果资产在UserData字段中定义了标签，则该属 `aria-label` 性会使用此类标签的值进行设置。

显示色板的组件具有将属 `listbox` 性设 `aria-label` 置为该组件本地化符号值的 `LABEL` 角色。 各个色板具有用于描 `option` 述集 `aria-setsize` 中的色 `aria-posinset` 板位置的具有和属性的角色。 如果选择了色板，则其属性 `aria-selected` 将设置为 `true`。
