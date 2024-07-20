---
title: 交互式数据支持
description: 交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式样本。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# 交互式数据支持{#interactive-data-support}

交互式视频查看器支持根据作为配置参数传递给查看器的交互式数据渲染交互式样本。

当前可见的样本对应于与其关联的视频时间区域。 单击或点按交互式样本会触发在创作时分配给它的操作。

交互式样本可以通过触发JavaScript回调在托管网页上激活快速视图，也可以将用户重定向到外部网页。

## 关于概览 {#section-7990e44f641042d2a38ba20c9413b3f8}

此类交互式样本应使用Adobe Experience Manager Assets - On-demand中的操作类型“quickview”进行创作。 当用户激活此类样本时，查看器运行`quickViewActivate` JavaScript回调并将样本数据传递给它。 嵌入网页应侦听此回调，并在触发时，页面打开其自己的概览实施。

## 重定向到外部网页 {#section-32ebe3c3a7f74892a428c5d48801de4d}

Experience Manager Assets中为操作类型“快速视图”创作的样本 — 按需将用户重定向到外部URL。 根据创作时的设置，URL可以在新的浏览器选项卡中、同一窗口中或在指定的浏览器窗口中打开。
