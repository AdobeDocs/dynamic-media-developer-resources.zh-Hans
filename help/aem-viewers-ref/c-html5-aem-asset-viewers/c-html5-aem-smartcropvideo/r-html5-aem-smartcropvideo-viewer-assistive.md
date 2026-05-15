---
title: 辅助技术支持
description: 所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
TQID: 'https://experienceleague.adobe.com/obdWIz9XkQQ9RCpfejLJrjVKKxCoPK3Qt-rW1BXad20'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# 辅助技术支持{#assistive-technology-support}

所有查看器组件都支持ARIA（可访问的富互联网应用程序）角色和属性，以改进与屏幕阅读器等辅助技术的集成。

顶层查看器元素具有默认设置为查看器名称的角色`region`和`aria-label`属性。 您可以使用`Container.LABEL`本地化符号控制标签。

按钮具有角色`button`和使用`aria-label`属性设置的描述性文本。 `aria-label`属性的值由按钮本地化符号的值填充。 禁用某个按钮时，将相应地设置`aria-disabled`属性。

滑块组件的角色`slider`具有属性`aria-valuenow`、`aria-valuemin`和`aria-valuemax`，用于描述当前滑块位置。

下拉列表由按钮激活，这些按钮具有设置为`true`的其他`aria-haspopup`属性和引用实际下拉面板元素的`aria-controls`属性。 下拉面板本身的角色为`menu`，子元素的角色为`menuitem`。 每个菜单项都指定了`aria-label`属性。

模式对话框具有角色`dialog`。 对话框的标头元素由`aria-labelledby`属性引用。
