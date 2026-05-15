---
title: 媒体集响应
description: 此部分中的设置适用于通过req=set修饰符获取的媒体集响应。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
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
