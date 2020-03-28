---
description: 预载图像是一个静态资源预览图像，它在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预载图像的目的是以可视方式缩短查看器加载时间并快速向用户展示内容。
seo-description: 预载图像是一个静态资源预览图像，它在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预载图像的目的是以可视方式缩短查看器加载时间并快速向用户展示内容。
seo-title: 预载图像
solution: Experience Manager
title: 预载图像
topic: Dynamic media
uuid: cb5db16d-b496-40e4-b8ef-5573c42d2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 预载图像{#preload-image}

预载图像是一个静态资源预览图像，它在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预载图像的目的是以可视方式缩短查看器加载时间并快速向用户展示内容。

预载图像非常适合最常见的查看器嵌入方法，即具有无限制高度的响应式嵌入。 请参阅标题无 [限制的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

但是，当使用其他嵌入方法或特定配置选项时，该功能具有某些限制。 在以下情况下，预载图像可能无法正确呈现：

* 当查看器的大小固定且大小是使用查看器预设记录内的配置属性或顶级查看器容器元素的外部查看器CSS文件中的配置属性定义的时候。 `stagesize`
* 当使用具有宽度和高度定义的查看器嵌入方法的灵活大小嵌入时。 请参阅标题 [定义了宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在以上列出的操作模式之一中使用查看器， `preloadImage` 则可能需要使用配置属性来禁用预载图像功能。

此外，即使在配置中启用预载图像，也不会使用预载图像——如果查看器嵌入到DOM元素中，则使用 `display:none` CSS设置将其隐藏或从DOM树中分离。
