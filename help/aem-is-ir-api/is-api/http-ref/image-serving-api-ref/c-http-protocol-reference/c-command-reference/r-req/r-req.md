---
description: 請求類型. 指定要求的型別。
solution: Experience Manager
title: 需要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 15%

---

# 需要{#req}

請求類型. 指定要求的型別。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`选项`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [影像集](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [地图](r-map-req.md)
* [遮色片](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [消息](r-message.md)
* [prop](r-props.md)
* [解决](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [设置](r-set.md)
* [目标](r-targets.md)
* [tmb](r-tmb.md)
* [使用者資料](r-userdata.md)
* [确认](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非在詳細描述中另有說明，否則伺服器會傳回 `text` 具有MIME型別的回應 `text/plain`. 許多請求型別可讓您指定回應型別，例如 `text`，這通常是預設值， `javascript`， `xml`，或 `json`. 相關的回應MIME型別為 `text/plain`， `text/javascript`， `text/xml`、和 `text/javascript`（分別）。

除非另有說明，否則回應會將回應格式化為一組 `name=value` 配對。

另請參閱 [屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
