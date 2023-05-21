---
description: 設定屬性是直接在Responsive影像資料庫管理的IMG元素上定義為屬性。 每個影像可以有自己的一組屬性。
solution: Experience Manager
title: 命令參考 — 組態屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# 命令參考 — 組態屬性{#command-reference-configuration-attributes}

設定屬性是直接在Responsive影像資料庫管理的IMG元素上定義為屬性。 每個影像可以有自己的一組屬性。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

可选.

「影像伺服」提供之影像的URL。 如果URL不存在，程式庫會使用在中設定的值 `src` 屬性做為遞補內容。 此屬性會提供初始影像和Responsive影像庫從不同位置管理的動態影像。

**示例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

若 `data-src` 已設定， `src` 是選用專案，可包含您要新增的任何URL。 例如，資料庫可包含的URL與「影像伺服」所使用影像相同。 或者，它可以包含GIF預留位置或甚至資料URI，以避免啟動時額外的伺服器來回行程。

若 `data-src` 未設定， `src` 為必填專案，且必須包含「影像伺服」提供之影像的URL。

**示例**

將資料URI用於 `src` 的屬性和影像伺服URL `data-src` 屬性：

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 資料中斷點 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

以逗號分隔的中斷點清單，並選擇性地後面加上冒號( `:`)，以及「影像伺服」命令或影像預設集。 每個中斷點是以邏輯CSS畫素定義的影像寬度值。 程式庫會從清單載入數值最近的影像，並在使用者端上縮小該影像，以符合執行階段CSS影像寬度。 （如果您在高密度熒幕上工作，從伺服器載入的影像轉譯會以中斷點值乘以裝置的畫素比表示）。

對於清單中的任何中斷點，都可以定義一或多個「影像伺服」命令或「影像預設集」名稱。 只有在這個特定中斷點目前作用中時，才會將這類額外引數套用至影像。

您可以使用任何支援的「影像伺服」命令，但會影響回應影像大小的檢視命令除外，例如 `wid=`， `hei=`，或 `scl=`. 相同的限制適用於影像預設集：搭配Responsive Image Library使用的影像預設集不得包含這類命令。

多個「影像伺服」命令或影像預設集名稱會以「」分隔 `&`「字元。 如果「影像伺服」命令的值中有逗號，此類逗號會取代為 `%2C`. 影像預設集名稱會以美元符號( `$`)。

**示例**

**僅使用中斷點**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**使用影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**使用影像預設集**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**使用影像預設集和影像伺服命令**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 資料模式 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

下列兩種智慧型裁切模式適用於AEM 6.4及更高版本和Dynamic Media Viewers 5.9及更高版本：

* **手動**  — 使用者定義的中斷點和對應的影像服務命令會在影像元素的屬性內定義。
* **智慧型裁切**  — 系統會自動從傳遞伺服器擷取運算智慧型裁切轉譯。 最佳轉譯是使用影像元素的執行階段大小來選取。

若要使用智慧型裁切模式，請設定 `data-mode` 屬性至 `smart crop`.

**示例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

關聯的影像元素會傳送 `s7responsiveViewer` 執行階段中斷點變更時的事件。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
