---
description: 交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。
seo-description: 交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。
seo-title: 交互式数据支持
solution: Experience Manager
title: 交互式数据支持
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# 交互式数据支持{#interactive-data-support}

交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。

当前可见的色板对应于与之关联的视频时间区域。 单击或点按交互式色板会触发在创作时分配给它的操作。

交互式色板可以通过触发JavaScript回调来激活托管网页上的快速视图，也可以将用户重定向到外部网页。

## 关于快速视图 {#section-7990e44f641042d2a38ba20c9413b3f8}

应使用AEM资产中的操作类型“quickview”按需创作这些类型的交互式色板。 当用户激活此样本时，查看器将运行 `quickViewActivate` JavaScript回调并将样本数据传递给它。 预期嵌入网页会监听此回调，当它触发时，该页面会打开自己的快速视图实现。

## 重定向到外部网页 {#section-32ebe3c3a7f74892a428c5d48801de4d}

为AEM资产中的操作类型“quickview”创作的色板——按需将用户重定向到外部URL。 根据创作时的设置，URL可以在新的浏览器选项卡中、在同一窗口中或在指定的浏览器窗口中打开。
