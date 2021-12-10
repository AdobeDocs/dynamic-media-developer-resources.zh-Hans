---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（无障碍的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性。 您可以使用 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本集 `aria-label` 属性。 的值 `aria-label` 属性会从按钮的本地化符号的值填充。 禁用按钮时， `aria-disabled` 属性会相应地进行设置。

主视图具有角色 `application`. 有关主视图的简要说明，请参阅 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，则使用提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产在UserData字段中定义了标签，则 `aria-label` 属性的值。

热点、区域和图像映射具有作用 `button` 描述性文本集 `aria-label` 属性，以及热点或图像映射标签的值。 当用户将焦点放在热点或图像映射上时，会使用 `aria-describedby`，其中使用提示的文本来自 `USAGE_HINT` 本地化符号。

缩略图具有角色 `dialog` with `aria-label` 由控制的属性 `ThumbnailGridView.LABEL` 本地化符号。 单个缩略图具有角色 `button`. 如果选择了缩略图，则会 `aria-selected` 属性设置为 `true`.

显示色板的组件具有角色 `listbox` with `aria-label` 属性设置为 `LABEL` 该组件的本地化符号。 单个色板具有 `option` with `aria-setsize` 和 `aria-posinset` 属性来描述集中的色板位置。 如果选择了色板，则会获得 `aria-selected` 属性设置为 `true`.

下拉列表由包含其他 `aria-haspopup` 属性设置为 `true` 和 `aria-controls` 引用实际下拉面板元素的属性。 下拉面板本身具有角色 `menu` 具有角色的子元素 `menuitem`. 每个菜单项都具有 `aria-label` 属性。

模式对话框具有角色 `dialog`. 对话框的标题元素被 `aria-labelledby` 属性。
