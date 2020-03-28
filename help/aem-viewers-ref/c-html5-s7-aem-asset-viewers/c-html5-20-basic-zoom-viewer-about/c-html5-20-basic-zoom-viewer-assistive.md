---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 99fdb4fd-5a3d-4c4e-b1c5-10651c08bf39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

按钮的角色和描 `button` 述性文本设置有属性 `aria-label` 属性。 属性的 `aria-label` 值由按钮的本地化符号的值填充。 当按钮被禁用时，属性 `aria-disabled` 会相应地设置。

主要视图有作用 `application`. 在中提供了主视图的简短描述 `aria-roledescription`，其值由相应主视图组件的 `ROLE_DESCRIPTION` 本地化符号定义。 为键盘用户提供的导航提示 `aria-describedby`使用，使用提示的文本来自本地化 `USAGE_HINT` 符号。 如果资产在UserData字段中定义了标签，则该属 `aria-label` 性会使用此类标签的值进行设置。
