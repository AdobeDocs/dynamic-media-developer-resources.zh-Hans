---
description: 此部分中的设置适用于通过req=set修饰符获得的媒体集响应。
solution: Experience Manager
title: 媒体集响应
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 媒体集响应{#media-set-responses}

此部分中的设置适用于通过req=set修饰符获得的媒体集响应。

## PS：：fvctx.useCatalogRecordValidation — 缓存策略 {#section-9accb087d16548a988993bb30395a6f6}

此属性在确定是否需要重新生成从缓存检索的响应时，控制缓存策略。 如果属性被禁用，则时间戳 [!DNL catalog.ini] 文件用于验证。 如果启用了属性，则最新的 `catalog::LastModified` 使用来自所有引用记录的时间戳进行验证。

## PS：：fvctx.nestingLimit — 嵌套限制 {#section-280210341f1647fea02590e7069934d2}

任何项目的最大嵌套深度 `req=set` 响应。 如果超过此深度，则会返回错误。

## PS：：fvctx.brochureLimit — 手册限制 {#section-fe36e47db49244cea7f07e9dd3639440}

中电子目录手册的最大数量 `req=set` 包含所有关联元数据的响应。 一旦超过此限制，将禁止与宣传册项目关联的任何专用映射和用户数据。
