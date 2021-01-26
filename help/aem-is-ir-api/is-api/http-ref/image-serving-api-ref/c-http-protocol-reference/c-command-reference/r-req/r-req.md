---
description: 請求類型. 指定请求的类型。
seo-description: 請求類型. 指定请求的类型。
seo-title: req
solution: Experience Manager
title: req
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 16%

---


# req{#req}

請求類型. 指定请求的类型。

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`选项`*]`

* [目录属性](r-catalogprops.md)
* [存在](r-exists.md)
* [imageprops](r-imageprops.md)
* [图像集](r-imageset-req.md)
* [img](r-img.md)
* [加载缓存](r-loadcache.md)
* [地图](r-map-req.md)
* [遮罩](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [消息](r-message.md)
* [prop](r-props.md)
* [解决](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [设置](r-set.md)
* [目标](r-targets.md)
* [tmb](r-tmb.md)
* [用户数据](r-userdata.md)
* [确认](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非详细说明中另有说明，否则服务器将返回MIME类型为`text/plain`的`text`响应。 许多请求类型允许您指定响应类型，如`text`，通常是默认类型`javascript`、`xml`或`json`。 关联的响应MIME类型分别为`text/plain`、`text/javascript`、`text/xml`和`text/javascript`。

除非另外说明，否则响应会将响应格式化为一组`name=value`对。

请参阅[属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
