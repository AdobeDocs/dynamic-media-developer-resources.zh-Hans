---
description: 交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。
seo-description: 交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。
seo-title: 交互式数据支持
solution: Experience Manager
title: 交互式数据支持
topic: Dynamic Media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# 交互式数据支持{#interactive-data-support}

交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式色板。

当前可见的色板与与之关联的视频时间区域相对应。 单击或点按交互式色板会触发在创作时分配给它的操作。

交互式色板可以通过触发JavaScript回调在托管网页上激活快速视图，也可以将用户重定向到外部网页。

## 关于快速视图{#section-7990e44f641042d2a38ba20c9413b3f8}

应使用AEM Assets（按需）中的操作类型“quickview”创作这些类型的交互式色板。 当用户激活此样板时，查看器将运行`quickViewActivate` JavaScript回调并将样板数据传递给它。 预期嵌入网页会监听此回调，当触发该回调时，该页面会打开自己的快速视图实现。

## 重定向到外部网页{#section-32ebe3c3a7f74892a428c5d48801de4d}

为AEM Assets的操作类型“quickview”创作的色板——按需将用户重定向到外部URL。 根据创作时的设置，URL可以在新的浏览器选项卡、同一窗口或指定的浏览器窗口中打开。
