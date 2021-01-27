---
description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-description: 所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
seo-title: 辅助技术支持
solution: Experience Manager
title: 辅助技术支持
topic: Dynamic Media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富Internet应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶级查看器元素具有角色`region`和`aria-label`属性，默认情况下该属性设置为查看器的名称。 可以使用`Container.LABEL`本地化符号控制标签。

主视图具有角色`application`。 在`aria-roledescription`中提供了主视图的简短描述，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则`aria-label`属性将设置为此类标签的值。

热点、区域和图像映射具有角色`button`和使用`aria-label`属性设置的描述性文本，其值为热点或图像映射标签。 当用户将焦点放在热点或图像地图上时，键盘用户的导航提示会使用`aria-describedby`提供，使用提示的文本来自`USAGE_HINT`本地化符号。
