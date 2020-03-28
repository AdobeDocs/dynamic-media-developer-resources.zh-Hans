---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

主要视图有作用 `application`. 在中提供了主视图的简短描述 `aria-roledescription`，其值由相应主视图组件的 `ROLE_DESCRIPTION` 本地化符号定义。 为键盘用户提供的导航提示 `aria-describedby`使用，使用提示的文本来自本地化 `USAGE_HINT` 符号。 如果资产在UserData字段中定义了标签，则该属 `aria-label` 性会使用此类标签的值进行设置。

热点、区域和图像映射具有角色和描述性文 `button` 本集，该文本集具有属 `aria-label` 性，并具有热点或图像映射标签的值。 当用户将焦点放在热点或图像地图上时，使用为键盘用户提供导航提示 `aria-describedby`，其中用于使用提示的文本来自本地化符 `USAGE_HINT` 号。
