---
title: 预载图像
description: 预载图像是静态资产预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是为了从视觉上改善查看器的加载时间并快速向用户呈现内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 预载图像{#preload-image}

预载图像是静态资产预览图像，在调用init()方法后立即加载，并在下载查看器SDK库、资产和预设信息时显示。 预加载图像的目的是为了从视觉上改善查看器的加载时间并快速向用户呈现内容。

预加载图像适用于最常见的查看器嵌入方法，即不受高度限制的响应式嵌入。 查看标题 [高度不受限制的响应式设计嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

但是，当使用其他嵌入方法或特定配置选项时，该功能有一定的限制。 在以下情况下，预加载图像可能无法正确呈现：

* 当查看器的大小固定并且大小使用以下任一方式定义时： `stagesize` 查看器预设记录中的配置属性。 或者，对顶级查看器容器元素使用外部查看器CSS文件。
* 使用宽度和高度定义的灵活尺寸嵌入查看器嵌入方法时。 查看标题 [定义宽度和高度的灵活大小嵌入](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

使用禁用预加载图像功能 `preloadImage` 配置属性。

此外，即使已在配置中启用预加载图像，也不使用预加载图像，前提是查看器嵌入到DOM元素中，并使用隐藏 `display:none` CSS设置或从DOM树分离。
