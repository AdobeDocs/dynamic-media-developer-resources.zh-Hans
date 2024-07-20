---
title: 媒体集响应
description: 此部分中的设置适用于通过req=set修饰符获取的媒体集响应。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 媒体集响应{#media-set-responses}

此部分中的设置适用于由`req=set`修饰符获取的媒体集响应。

## PS：：fvctx.useCatalogRecordValidation — 缓存策略 {#section-9accb087d16548a988993bb30395a6f6}

此属性控制在确定是否必须重新生成从缓存检索的设置响应时的缓存策略。 如果属性被禁用，则使用[!DNL catalog.ini]文件的时间戳进行验证。 如果启用了属性，将使用所有引用记录中的最新`catalog::LastModified`时间戳进行验证。

## PS：：fvctx.nestingLimit — 嵌套限制 {#section-280210341f1647fea02590e7069934d2}

任何`req=set`响应的最大嵌套深度。 如果超过此深度，则会返回错误。

## PS：：fvctx.brochureLimit — 宣传册限制 {#section-fe36e47db49244cea7f07e9dd3639440}

包含所有关联元数据的`req=set`响应中的eCatalog宣传册的最大数量。 一旦超过此限制，将禁止与小册子项目关联的任何专用映射和用户数据。
