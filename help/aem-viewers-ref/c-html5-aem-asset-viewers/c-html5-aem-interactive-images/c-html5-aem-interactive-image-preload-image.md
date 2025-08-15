---
title: 预加载图像
description: 预加载图像是一种静态资源预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预加载图像的目的在于直观地改善查看者的加载时间并向用户快速展示内容。
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

预加载图像是一种静态资源预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资源和预设信息时显示。 预加载图像的目的在于直观地改善查看者的加载时间并向用户快速展示内容。

预加载图像适用于最常见的查看器嵌入方法，即不受高度限制的响应式嵌入。 查看标题[具有不受限制高度的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

但是，当使用其他嵌入方法或特定配置选项时，该功能有一定的限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器大小固定且大小在查看器预设记录中使用`stagesize`配置属性定义时。 或者，对顶级查看器容器元素使用外部查看器CSS文件。
* 使用灵活大小嵌入时，采用宽度和高度定义的查看器嵌入方法。 查看标题[宽度和高度定义的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

如果您在上面列出的操作模式之一中使用查看器，请使用`preloadImage`配置属性禁用预加载图像功能。

此外，如果查看器嵌入到DOM元素中使用`display:none` CSS设置是隐藏的，或者已从DOM树中分离，则不会使用预加载图像（即使在配置中启用了预加载图像）。
