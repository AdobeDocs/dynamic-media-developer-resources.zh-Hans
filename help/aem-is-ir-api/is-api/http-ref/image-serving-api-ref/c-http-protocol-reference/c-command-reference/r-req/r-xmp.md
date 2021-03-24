---
description: XMP元数据。 返回与在请求路径中指定的图像关联的XMP元数据。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 12%

---


# xmp{#xmp}

XMP元数据。 返回与在请求路径中指定的图像关联的XMP元数据。

`req=xmp`

其他命令将被忽略。 UTF-8编码适用。 响应的格式为MIME类型为`text/xml`的XML。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

## 属性 {#section-0d26b6a56c844153ae5cea4880370d00}

请求属性。 无论当前图层设置如何，均适用。

## 默认 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

如果URL不包括图像路径或修饰符，则：

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否则，`req=img`

## 示例 {#section-34213692deab4a0f9037d5844132ee14}

查询图像文件属性。

` http:// *`伺服器`*/myPath/myImage.tif?req=imageprops`

查询图像目录属性：

` http:// *`伺服器`*/myRootId?req=catalogprops`

从嵌入在HTML文件中的客户端JavaScript访问图像目录条目的属性：

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

检索特定目录条目的蒙版图像，并缩放到原始大小的25%:

` http:// *`伺服器`*/myRootId/myImageId?req=mask&scale=0.25`

以八分之一的大小请求图像：

` http:// *`伺服器`*/myRootId/myImageId?scl=8`

这与：

` http:// *`伺服器`*/myRootId/myImageId?req=img&scl=8`

请求图像的缩略图，具体取决于在图像目录中指定的缩略图属性：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

向服务器日志发送文本消息：

` http:// *`伺服器`*/myRootId?req=message&message=This%20is%20the%20message`

## 另请参阅 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [目录：:目标](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)，目 [录：:UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)，缩 [放缩图](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) [,属性,图像图](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
