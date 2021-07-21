---
description: 本节中的设置适用于通过req=set修饰符获取的媒体集响应。
solution: Experience Manager
title: 媒体集响应
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# 媒体集响应{#media-set-responses}

本节中的设置适用于通过req=set修饰符获取的媒体集响应。

## PS::fvctx.useCatalogRecordValidation — 缓存策略 {#section-9accb087d16548a988993bb30395a6f6}

此属性在确定是否需要重新生成从缓存中检索的响应时控制缓存策略。 如果禁用了属性，则将使用[!DNL catalog.ini]文件的时间戳进行验证。 如果启用了属性，则所有引用记录的最新`catalog::LastModified`时间戳将用于验证。

## PS::fvctx.nestingLimit — 嵌套限制 {#section-280210341f1647fea02590e7069934d2}

任何`req=set`响应的最大嵌套深度。 如果超出此深度，则返回错误。

## PS::fvctx.brochureLimit — 手册限制 {#section-fe36e47db49244cea7f07e9dd3639440}

`req=set`响应中包含所有关联元数据的电子目录小册子的最大数量。 一旦超过此限制，与手册项目关联的任何专用地图和用户数据都将被禁止。
