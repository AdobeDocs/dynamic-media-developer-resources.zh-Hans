---
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
title: 辅助技术支持
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色 `region` 和 `aria-label` 属性默认设置为查看器的名称。 您可以使用以下内容控制标签 `Container.LABEL` 本地化符号。

按钮具有角色 `button` 和描述性文本设置 `aria-label` 属性。 的值 `aria-label` 属性填充自按钮本地化符号的值。 禁用某个按钮后， `aria-disabled` 属性会进行相应的设置。

主视图具有角色 `application`. 中提供了主视图的简要说明 `aria-roledescription`，其值由 `ROLE_DESCRIPTION` 相应主视图组件的本地化符号。 为键盘用户提供的导航提示使用 `aria-describedby`，用法提示的文本来自 `USAGE_HINT` 本地化符号。 如果资产的UserData字段中定义了标签，则 `aria-label` 属性被设置为此类标签的值。

热点、区域和图像映射将发挥作用 `button` 和描述性文本集 `aria-label` 属性，其值为热点或图像映射标签。 当用户重点关注热点或图像映射时，可以使用为键盘用户提供导航提示 `aria-describedby`，使用提示的文本来自 `USAGE_HINT` 本地化符号。

缩略图具有角色 `dialog` 替换为 `aria-label` 属性由控制 `ThumbnailGridView.LABEL` 本地化符号。 单个缩略图具有角色 `button`. 如果选择了缩略图，则会获得 `aria-selected` 属性设置为 `true`.

显示样本的组件具有此角色 `listbox` 替换为 `aria-label` 属性设置为的值 `LABEL` 该组件的本地化符号。 单个样本具有此角色 `option` 替换为 `aria-setsize` 和 `aria-posinset` 属性，用于描述样本集内的样本位置。 如果选择了样本，它将获得 `aria-selected` 属性设置为 `true`.

下拉列表由具有其他功能的按钮激活 `aria-haspopup` 属性设置为 `true` 和 `aria-controls` 引用实际下拉面板元素的属性。 下拉面板本身具有角色 `menu` 具有子元素角色 `menuitem`. 每个菜单项都具有 `aria-label` 指定的属性。

搜索用户界面使用角色分组在元素中 `search`. 搜索输入字段具有角色 `searchbox` 和引用了由以下对象控制的信息性标签 `SearchPanel.INFO_PROMPT` 本地化符号 `aria-describedby` 属性。

模式对话框具有角色 `dialog`. 对话框的标头元素由 `aria-labelledby` 属性。
