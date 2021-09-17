---
title: 预加载图像
description: 预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 预加载图像{#preload-image}

预加载图像是一种静态资产预览图像，它在调用init()方法后直接加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是直观地缩短查看者加载时间并快速向用户呈现内容。

预加载图像非常适合于最常用的查看器嵌入方法，即具有无限制高度的响应嵌入。 请参阅标题[具有不受限高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)。

但是，当使用其他嵌入方法或特定配置选项时，该功能存在某些限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器的大小固定且大小是使用查看器预设记录内的`stagesize`配置属性定义的，或者在顶级查看器容器元素的外部查看器CSS文件中定义的。
* 在查看器嵌入的宽度和高度定义方法中使用灵活的大小嵌入时。 请参阅标题[定义了宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果在上面列出的操作模式之一中使用查看器，请使用`preloadImage`配置属性禁用预加载图像功能。

此外，即使在配置中启用了预加载图像，也不会使用预加载图像 — 如果查看器已嵌入到DOM元素中，则会使用`display:none` CSS设置进行隐藏，或从DOM树中分离查看器。
