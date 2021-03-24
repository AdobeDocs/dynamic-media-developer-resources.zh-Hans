---
description: 预加载图像是一个静态资源预览图像，它在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预载图像的目的是直观地缩短查看器加载时间并快速向用户呈现内容。
solution: Experience Manager
title: 预载图像
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 预载图像{#preload-image}

预加载图像是一个静态资源预览图像，它在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预载图像的目的是直观地缩短查看器加载时间并快速向用户呈现内容。

预载图像对于最常见的查看器嵌入方法（即具有无限制高度的响应式嵌入）效果不错。 请参阅标题[具有无限高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，当使用其他嵌入方法或特定配置选项时，该功能具有某些限制。 在以下情况下，预载图像可能无法正确呈现：

* 当查看器的大小固定且大小是使用查看器预设记录内的`stagesize`配置属性或顶级查看器容器元素的外部查看器CSS文件中定义的。
* 当使用带有查看器嵌入的宽度和高度定义的灵活大小嵌入时。 请参阅标题[定义了宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上述操作模式之一中使用查看器，则可能需要使用`preloadImage`配置属性禁用预载图像功能。

此外，即使在配置中启用预载图像，也不会使用预载图像 — 如果查看器已嵌入到DOM元素中，则使用`display:none` CSS设置进行隐藏，或从DOM树中分离。
