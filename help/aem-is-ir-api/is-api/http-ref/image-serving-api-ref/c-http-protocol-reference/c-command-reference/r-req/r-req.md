---
description: 請求類型. 指定请求的类型。
solution: Experience Manager
title: 请求
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---

# 请求{#req}

請求類型. 指定请求的类型。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`选项`*]`

* [catalogprops](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [图像集](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [地图](r-map-req.md)
* [蒙版](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [消息](r-message.md)
* [prop](r-props.md)
* [解决](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [设置](r-set.md)
* [目标](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [确认](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非在详细描述中另有说明，否则服务器会返回MIME类型为`text/plain`的`text`响应。 许多请求类型都允许您指定响应类型，如`text`，该类型通常为默认类型：`javascript`、`xml`或`json`。 关联的响应MIME类型分别为`text/plain`、`text/javascript`、`text/xml`和`text/javascript`。

除非另有说明，否则响应会将响应格式化为一组`name=value`对。

请参阅[属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
