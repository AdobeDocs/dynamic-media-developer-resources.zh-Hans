---
description: XMP中繼資料。 傳回與要求路徑中所指定影像相關聯的XMP中繼資料。
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 12%

---

# xmp{#xmp}

XMP中繼資料。 傳回與要求路徑中所指定影像相關聯的XMP中繼資料。

`req=xmp`

其他指令會被忽略。 UTF-8編碼適用。 回應會格式化為具有MIME型別的XML `text/xml`.

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

## 屬性 {#section-0d26b6a56c844153ae5cea4880370d00}

要求屬性。 無論目前的圖層設定為何，均適用。

## 默认 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

如果URL不包含影像路徑或修飾元，則：

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否則， `req=img`

## 示例 {#section-34213692deab4a0f9037d5844132ee14}

查詢影像檔案屬性。

` http:// *`伺服器`*/myPath/myImage.tif?req=imageprops`

查詢影像目錄屬性：

` http:// *`伺服器`*/myRootId?req=catalogprops`

從內嵌於HTML檔案中的使用者端JavaScript存取影像目錄專案的屬性：

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

擷取特定目錄專案的遮色片影像，縮放為原始大小的25%：

` http:// *`伺服器`*/myRootId/myImageId?req=mask&scale=0.25`

請求八分之一大小的影像：

` http:// *`伺服器`*/myRootId/myImageId?scl=8`

這與：

` http:// *`伺服器`*/myRootId/myImageId?req=img&scl=8`

根據影像目錄中指定的縮圖屬性，請求影像的縮圖：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

傳送文字訊息至伺服器記錄檔：

` http:// *`伺服器`*/myRootId?req=message&message=This%20is%20the%20message`

## 另请参阅 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [catalog：：目標](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)， [catalog：：UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)， [縮圖縮放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)， [屬性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)， [影像地圖](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
