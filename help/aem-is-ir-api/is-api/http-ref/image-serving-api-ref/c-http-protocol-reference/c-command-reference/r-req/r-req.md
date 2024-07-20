---
description: 请求类型。 指定请求的类型。
solution: Experience Manager
title: 需要
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# 需要{#req}

请求类型。 指定请求的类型。

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
* [用户数据](r-userdata.md)
* [确认](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

除非在详细说明中另有说明，否则服务器返回MIME类型为`text/plain`的`text`响应。 许多请求类型允许您指定响应类型，例如通常是默认的`text`、`javascript`、`xml`或`json`。 关联的响应MIME类型分别为`text/plain`、`text/javascript`、`text/xml`和`text/javascript`。

除非另有说明，否则响应会将响应格式化为一组`name=value`对。

查看[属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。
