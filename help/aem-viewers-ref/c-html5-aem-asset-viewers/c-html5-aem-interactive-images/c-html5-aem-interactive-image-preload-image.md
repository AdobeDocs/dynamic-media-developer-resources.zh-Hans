---
title: 预加载图像
description: 预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 预加载图像{#preload-image}

预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。

预加载图像非常适合于最常用的查看器嵌入方法，即具有无限制高度的响应嵌入。 请参阅标题[具有不受限高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

但是，当使用其他嵌入方法或特定配置选项时，该功能存在某些限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器的大小固定且大小是使用查看器预设记录内的`stagesize`配置属性定义的时。 或者，将外部查看器CSS文件用于顶级查看器容器元素。
* 在查看器嵌入的宽度和高度定义方法中使用灵活的大小嵌入时。 请参阅标题[定义了宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上面列出的操作模式之一中使用查看器，请使用`preloadImage`配置属性禁用预加载图像功能。

此外，即使在配置中启用了预加载图像，也不会使用预加载图像 — 如果查看器已嵌入到DOM元素中，则会使用`display:none` CSS设置进行隐藏，或从DOM树中分离查看器。
