---
title: 自訂Video360檢視器
description: Video360檢視器的所有視覺化自訂和大部分行為自訂都是透過建立自訂CSS來完成。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 0%

---

# 自訂Video360檢視器{#customizing-video-viewer}

Video360檢視器的所有視覺化自訂和大部分行為自訂都是透過建立自訂CSS來完成。

建議的工作流程是取用適當檢視器的預設CSS檔案、將其複製到不同位置、自訂該檔案，並在中指定自訂檔案的位置 `style=` 命令。

可在以下位置找到預設CSS檔案：

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

自訂CSS檔案必須包含與預設檔案相同的類別宣告。 如果省略類別宣告，則檢視器無法正常運作，因為它未提供使用者介面元素的內建預設樣式。

提供自訂CSS規則的替代方式是直接在網頁上或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記住檢視器會指派 `.s7video360viewer` 類別至其容器DOM元素。 如果您使用傳遞的外部CSS檔案 `style=` 命令，使用 `.s7video360viewer` 類別作為CSS規則之子系選擇器中的父類別。 如果您在網頁上執行內嵌樣式，請一併使用容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7video360viewer`

## 建立回應式設計CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

您可以在CSS中鎖定不同的裝置和內嵌大小，讓內容顯示方式因使用者裝置或特定網頁版面配置而異。 此方法包括但不限於不同的版面、使用者介面元素大小和圖稿解析度。

檢視器支援兩種建立回應式設計CSS的機制： CSS標籤和標準CSS媒體查詢。 您可以單獨或一起使用標籤或查詢。

**CSS標籤**

為協助建立回應式設計的CSS，檢視器支援CSS標籤。 這些標籤是特殊的CSS類別，會動態指派給頂層檢視器容器元素。 它們是根據執行階段檢視器大小和目前裝置使用的輸入型別。

第一組CSS標籤包括 `.s7size_large`， `.s7size_medium`、和 `.s7size_small` 類別。 它們會根據檢視器容器的執行階段區域套用。 如果檢視器區域等於或大於普通桌上型顯示器的大小，則 `.s7size_large` 使用；如果該區域靠近常見的平板電腦裝置，則 `.s7size_medium` 已指派。 若為類似行動電話熒幕的區域，則 `.s7size_small` 已設定。 這些CSS標籤的主要用途是為不同的熒幕和檢視器大小建立不同的使用者介面配置。

第二組CSS標籤包含 `.s7mouseinput` 和 `.s7touchinput`. 標籤 `.s7touchinput` 若目前裝置具備觸控輸入功能，則為設定；否則， `.s7mouseinput` 已使用。 這些標籤主要用於為不同的輸入型別建立具有不同熒幕大小的使用者介面輸入元素，因為通常觸控輸入需要更大的元素。 如果裝置同時具備滑鼠輸入和觸控功能， `.s7touchinput` 「 」已設定，且檢視器呈現觸控式好記的使用者介面。

下列範例CSS會在使用滑鼠輸入的系統上將播放/暫停按鈕大小設定為28x28畫素，在觸控裝置上將設定為56x56畫素。 此外，如果檢視器大小大幅縮減，則會完全隱藏按鈕：

```
.s7video360viewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7video360viewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7video360viewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

若要鎖定具有不同畫素密度的裝置，您必須使用CSS媒體查詢。 以下媒體查詢區塊將包含高密度熒幕專屬的CSS：

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建置回應式設計CSS的最靈活方式，因為這樣可讓您不僅鎖定裝置熒幕大小，而且鎖定實際檢視器大小，因為這對於回應式設計版面非常有用。

您可以使用預設檢視器CSS檔案作為CSS標籤方法的一個範例。

**CSS媒體查詢**

您也可以使用純CSS媒體查詢來完成裝置偵測。 指定媒體查詢區塊中包含的所有內容，只會在對應裝置上執行時套用。

套用至HTML5行動檢視器時，會依照下列順序使用四個CSS媒體查詢（定義於CSS中）：

1. 僅包含所有觸控裝置專屬的規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 僅包含具有高解析度熒幕的平板電腦專屬規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 僅包含所有行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 僅包含高解析度熒幕行動電話的特定規則。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒體查詢方法，您應該使用裝置感應來組織CSS，如下所示：

* 首先，案頭專屬區段會定義案頭專屬或所有畫面通用的所有屬性。
* 其次，這四個媒體查詢會依照上述定義的順序進行，並提供專屬於對應裝置型別的CSS規則。

不需要在每個媒體查詢中複製整個檢視器CSS。 只有在媒體查詢內重新定義指定裝置的特定屬性。

## CSS精靈 {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多檢視器使用者介面元素會使用點陣圖圖案來設定樣式，而且會有多個不同的視覺狀態。 一個很好的範例是按鈕，通常至少有三個不同的狀態：「向上」、「向上」和「向下」。 每個狀態都需要指定自己的點陣圖圖稿。

透過傳統樣式設定方法，CSS會針對使用者介面元素的每個狀態，對伺服器上的個別影像檔案提供個別參考。 以下為設定全熒幕按鈕樣式的CSS範例：

```
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

此方法的缺點在於，當元素首次互動時，一般使用者會遇到使用者介面回應閃爍或延遲的情況。 發生此動作是因為尚未下載新元素狀態的影像圖稿。 此外，由於對伺服器的HTTP呼叫數增加，此方法可能會對效能造成輕微的負面影響。

CSS sprite是一種不同的方法，所有元素狀態的影像圖稿會合併到稱為「sprite」的單一PNG檔案中。 此類「sprite」具有給定元素的所有視覺狀態，它們會一個接一個地放置。 在設定包含精靈的使用者介面元素的樣式時，會針對CSS中的所有不同狀態參考相同的Sprite影像。 此外， `background-position` 屬性會用於每個狀態，以指定使用「sprite」影像的哪個部分。 您可以以任何適當的方式建構「sprite」影像。 檢視器通常會垂直棧疊。 以下是以「sprite」為基礎的範例，說明如何更早設定相同全熒幕按鈕的樣式：

```
.s7video360viewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 一般樣式注意事項和建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS內外部資產的所有路徑都會根據CSS位置解析，而非檢視器HTML頁面位置。 將預設CSS複製到其他位置時，請注意此規則。 複製預設資產或更新自訂CSS內的路徑。
* 點陣圖稿的偏好格式為PNG。
* 點陣圖圖稿會使用指定給使用者介面元素 `background-image` 屬性。
* 此 `width` 和 `height` 使用者介面元素的屬性會定義其邏輯大小。 傳遞至的點陣圖大小 `background-image` 不會影響邏輯大小。

* 若要使用Retina等高解析度熒幕的高畫素密度，請指定兩倍於邏輯使用者介面元素大小的點陣圖圖稿。 然後，套用 `-webkit-background-size:contain` 屬性，將背景縮小至邏輯使用者介面元素大小。
* 若要從使用者介面移除按鈕，請新增 `display:none` 至其CSS類別。
* 您可以對CSS支援的顏色值使用各種格式。 如果您需要透明度，請使用格式 `rgba(R,G,B,A)`. 否則，您可以使用格式 `#RRGGBB`.

* 使用CSS自訂檢視器使用者介面時，請使用 `!IMPORTANT` 樣式檢視器元素不支援規則。 尤其是， `!IMPORTANT` 規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行階段樣式。 原因是它可能會影響適當元件的行為。 您應該改用具有適當特性的CSS選取器，以設定本參考指南中記錄的CSS屬性。

## 常見使用者介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是適用於Video360檢視器的使用者介面元素參考檔案：
