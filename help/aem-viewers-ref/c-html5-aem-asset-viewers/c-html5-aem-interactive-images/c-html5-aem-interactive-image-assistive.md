---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

主视图具有角色`application`。 `aria-roledescription`中提供了主视图的简短说明，其值由相应主视图组件的`ROLE_DESCRIPTION`本地化符号定义。 使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。 如果资产在UserData字段中定义了标签，则会使用此类标签的值设置`aria-label`属性。

热点、区域和图像映射具有角色`button`和使用`aria-label`属性设置的描述性文本，并具有热点或图像映射标签的值。 当用户关注热点或图像映射时，使用`aria-describedby`为键盘用户提供导航提示，使用提示的文本来自`USAGE_HINT`本地化符号。
