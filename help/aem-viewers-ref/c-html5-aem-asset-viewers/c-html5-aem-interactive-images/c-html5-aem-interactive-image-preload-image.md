---
description: 预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。
solution: Experience Manager
title: 预加载图像
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,Business Practitioner
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 预加载图像{#preload-image}

预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。

预加载图像非常适合于最常用的查看器嵌入方法，即具有无限制高度的响应嵌入。 请参阅标题[具有不受限高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

但是，当使用其他嵌入方法或特定配置选项时，该功能存在某些限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器的大小固定且大小是使用查看器预设记录内或顶级查看器容器元素的外部查看器CSS文件中的`stagesize`配置属性定义的时。
* 当使用具有宽度和高度定义的查看器嵌入方法的柔性大小嵌入时。 请参阅标题[定义了宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上面列出的操作模式之一中使用查看器，则可能需要使用`preloadImage`配置属性来禁用预加载图像功能。

此外，即使在配置中启用了预加载图像，也不会使用预加载图像 — 如果查看器已嵌入到DOM元素中，则会使用`display:none` CSS设置进行隐藏，或从DOM树中分离查看器。
