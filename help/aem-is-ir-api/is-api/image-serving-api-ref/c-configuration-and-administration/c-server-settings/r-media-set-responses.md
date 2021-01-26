---
description: 本节中的设置适用于通过req=set修饰符获取的媒体集响应。
seo-description: 本节中的设置适用于通过req=set修饰符获取的媒体集响应。
seo-title: 媒体集响应
solution: Experience Manager
title: 媒体集响应
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# 媒体集响应{#media-set-responses}

本节中的设置适用于通过req=set修饰符获取的媒体集响应。

## PS::fvctx.useCatalogRecordValidation —— 缓存策略{#section-9accb087d16548a988993bb30395a6f6}

当确定是否需要重新生成从缓存检索的响应时，此属性控制缓存策略。 如果禁用了属性，则使用[!DNL catalog.ini]文件的时间戳进行验证。 如果启用了属性，则所有引用记录的最新`catalog::LastModified`时间戳将用于验证。

## PS::fvctx.nestingLimit —— 嵌套限制{#section-280210341f1647fea02590e7069934d2}

任何`req=set`响应的最大嵌套深度。 如果超出此深度，则返回错误。

## PS::fvctx.brochureLimit —— 手册限制{#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`响应中包含所有关联元数据的电子目录小册子的最大数量。 一旦超过此限制，与宣传册项目相关的任何私人地图和用户数据都被禁止。
