---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素的角色和属 `region` 性默 `aria-label` 认设置为查看器的名称。 您可以使用本地化符号控制标 `Container.LABEL` 签。

按钮的角色和描 `button` 述性文本设置有属性 `aria-label` 属性。 属性的 `aria-label` 值由按钮的本地化符号的值填充。 当按钮被禁用时，属性 `aria-disabled` 会相应地设置。

主要视图有作用 `application`. 在中提供了主视图的简短描述 `aria-roledescription`，其值由相应主视图组件的 `ROLE_DESCRIPTION` 本地化符号定义。 为键盘用户提供的导航提示 `aria-describedby`使用，使用提示的文本来自本地化 `USAGE_HINT` 符号。 如果资产在UserData字段中定义了标签，则该属 `aria-label` 性会使用此类标签的值进行设置。

热点、区域和图像映射具有角色和描述性文 `button` 本集，该文本集具有属 `aria-label` 性，并具有热点或图像映射标签的值。 当用户将焦点放在热点或图像地图上时，使用为键盘用户提供导航提示 `aria-describedby`，其中用于使用提示的文本来自本地化符 `USAGE_HINT` 号。

缩览图具有由 `dialog` 本地化 `aria-label` 符号控制的属性 `ThumbnailGridView.LABEL` 角色。 单个缩略图具有角色 `button`。 如果选择了缩略图，则会将其 `aria-selected` 属性设置为 `true`。

显示色板的组件具有将属 `listbox` 性设 `aria-label` 置为该组件本地化符号值的 `LABEL` 角色。 各个色板具有用于描 `option` 述集 `aria-setsize` 中的色 `aria-posinset` 板位置的具有和属性的角色。 如果选择了色板，则其属性 `aria-selected` 将设置为 `true`。

下拉列表由按钮激活，其他属性设 `aria-haspopup` 置为，属 `true` 性 `aria-controls` 引用实际的下拉面板元素。 下拉面板本身具有子元素 `menu` 具有角色的角色 `menuitem`。 每个菜单项都指定 `aria-label` 了属性。

搜索用户界面将在具有角色的元素中分组 `search`。 搜索输入字段具有角色， `searchbox` 并引用由具有属性的本地化符 `SearchPanel.INFO_PROMPT` 号控制的信息 `aria-describedby` 标签。

Modal对话框具有角色 `dialog`。 该对话框的标题元素由属性引 `aria-labelledby` 用。
