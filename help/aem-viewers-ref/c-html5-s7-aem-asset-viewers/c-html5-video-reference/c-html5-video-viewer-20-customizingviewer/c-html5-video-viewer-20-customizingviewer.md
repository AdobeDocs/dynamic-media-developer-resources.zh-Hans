---
title: 自訂視訊檢視器
description: 自訂視訊檢視器
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# 自訂視訊檢視器{#customizing-video-viewer}

所有視覺化自訂和大多數行為自訂都是透過建立自訂CSS完成的。

建議的工作流程是取用適當檢視器的預設CSS檔案、將其複製到不同位置、自訂該檔案，並在中指定自訂檔案的位置 `style=` 命令。

可在以下位置找到預設CSS檔案：

`<s7_viewers_root>/html5/VideoViewer.css`

自訂CSS檔案必須包含與預設檔案相同的類別宣告。 如果省略類別宣告，則檢視器無法正常運作，因為它未提供使用者介面元素的內建預設樣式。

提供自訂CSS規則的替代方式是直接在網頁上或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記得檢視器指派 `.s7videoviewer` 類別至其容器DOM元素。 如果您使用隨附的外部CSS檔案 `style=` 命令，使用 `.s7videoviewer` 類別作為CSS規則之子系選擇器中的父類別。 如果您在網頁上內嵌樣式，請一併使用容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7videoviewer`

## 建立回應式設計CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

您可以鎖定CSS中的不同裝置，使內容顯示方式因使用者裝置而異。 此目標定位包括但不限於不同的使用者介面元素大小和圖稿解析度。

檢視器支援兩種建立回應式設計CSS的機制： CSS標籤和標準CSS媒體查詢。 您可以單獨或一起使用這兩種機制。

**CSS標籤**

為協助您建立回應式設計CSS，檢視器支援CSS標籤，這些標籤會動態地指派特殊CSS類別給頂層檢視器容器元素。 指派是以執行階段檢視器大小和目前裝置使用的輸入型別為基礎。

第一組CSS標籤包括 `.s7size_large`， `.s7size_medium`、和 `.s7size_small` 類別。 它們會根據檢視器容器的執行階段區域套用。 也就是說，如果檢視器區域等於或大於一般桌上型電腦熒幕的大小 `.s7size_large` 使用；如果區域的大小接近一般平板電腦裝置 `.s7size_medium` 已指派。 對於類似行動電話熒幕的區域， `.s7size_small` 已設定。 這些CSS標籤的主要用途是為不同的熒幕和檢視器大小建立不同的使用者介面配置。

第二組CSS標籤包括 `.s7mouseinput` 和 `.s7touchinput`. 標籤 `.s7touchinput` 若目前裝置具備觸控輸入功能，則為設定；否則， `.s7mouseinput` 已使用。 這些標籤旨在為不同的輸入型別建立具有不同熒幕大小的使用者介面輸入元素，因為一般而言，觸控輸入需要更大的元素。 如果裝置同時具備滑鼠輸入和觸控功能， `.s7touchinput` 「 」已設定，且檢視器呈現觸控式好記的使用者介面。

下列範例CSS會在使用滑鼠輸入的系統上將播放/暫停按鈕大小設定為28 x 28畫素，在觸控裝置上將設定為56 x 56畫素。 此外，如果檢視器大小變得太小，則會完全隱藏按鈕：

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

若要鎖定具有不同畫素密度的裝置，請使用CSS媒體查詢。 下列媒體查詢區塊將包含高密度熒幕專屬的CSS：

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS標籤是建置回應式設計CSS的最靈活方式。 原因是因為它可讓您不僅鎖定裝置熒幕大小，還鎖定實際檢視器大小，這對於回應式設計頁面佈局可能很有用。

使用預設檢視器CSS檔案作為CSS標籤方法的一個範例。

**CSS媒體查詢**

裝置感應也可以使用純CSS媒體查詢來完成。 指定媒體查詢區塊中包含的所有內容，只會在對應裝置上執行時套用。

套用至行動檢視器時，請使用四個CSS媒體查詢，其定義順序如下（在CSS中）：

1. 僅包含所有觸控裝置專屬的規則。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

使用CSS媒體查詢方法時，您應該使用裝置感應來組織CSS，如下所示：

* 首先，案頭專屬區段會定義案頭專屬或所有畫面通用的所有屬性。
* 其次，這四個媒體查詢應該依照上述定義的順序進行，並提供對應裝置型別專屬的CSS規則。

不需要在每個媒體查詢中複製整個檢視器CSS。 只有在媒體查詢內重新定義指定裝置的特定屬性。

## CSS精靈 {#section-9b6d8d601cb441d08214dada7bb4eddc}

許多檢視器使用者介面元素會使用點陣圖圖案來設定樣式，而且會有多個不同的視覺狀態。 一個很好的範例是按鈕，通常至少有三個不同的狀態：「向上」、「向上」和「向下」。 每個狀態都需要指定自己的點陣圖圖稿。

透過傳統樣式設定方法，CSS會針對使用者介面元素的每個狀態，對伺服器上的個別影像檔案提供個別參考。 以下為設定全熒幕按鈕樣式的CSS範例：

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

此方法的缺點在於，當元素首次互動時，一般使用者會遇到使用者介面回應閃爍或延遲的情況。 發生此動作是因為尚未下載新元素狀態的影像圖稿。 此外，由於對伺服器的HTTP呼叫數增加，此方法可能會對效能造成輕微的負面影響。

CSS sprite是一種不同的方法，所有元素狀態的影像圖稿會合併到稱為「sprite」的單一PNG檔案中。 此類「sprite」具有給定元素的所有視覺狀態，它們會一個接一個地放置。 在設定包含精靈的使用者介面元素的樣式時，會針對CSS中的所有不同狀態參考相同的Sprite影像。 此外， `background-position` 屬性會用於每個狀態，以指定使用「sprite」影像的哪個部分。 您可以以任何適當的方式建構「sprite」影像。 檢視器通常會垂直棧疊。 以下是以上相同全熒幕按鈕樣式的「sprite」型範例：

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 一般樣式注意事項和建議 {#section-097418bd618740bba36352629e4d88e1}

* CSS內外部資產的所有路徑都是根據CSS位置而不是檢視器HTML頁面的位置來解析。 將預設CSS複製到其他位置時，請記得說明此規則。 複製自訂CSS內的預設資產或更新路徑。
* 點陣圖稿的偏好格式為PNG。
* 點陣圖圖稿會使用指定給使用者介面元素 `background-image` 屬性。
* 此 `width` 和 `height` 使用者介面元素的屬性會定義其邏輯大小。 傳遞至的點陣圖大小 `background-image` 不會影響邏輯大小。

* 若要使用Retina等高解析度熒幕的高畫素密度，請指定兩倍於邏輯使用者介面元素大小的點陣圖圖稿。 然後，套用 `-webkit-background-size:contain` 屬性，將背景縮小至邏輯使用者介面元素大小。
* 若要從使用者介面移除按鈕，請新增 `display:none` 至其CSS類別。
* 您可以對CSS支援的顏色值使用各種格式。 如果您需要透明度，請使用格式 `rgba(R,G,B,A)`. 否則，您可以使用格式 `#RRGGBB`.

* 使用CSS自訂檢視器使用者介面時，請使用 `!IMPORTANT` 樣式檢視器元素不支援規則。 尤其是， `!IMPORTANT` 規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行階段樣式。 原因是它可能會影響適當元件的行為。 您應該改用具有適當特性的CSS選取器，以設定本參考指南中記錄的CSS屬性。

## 常見使用者介面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是適用於Video Viewer的使用者介面元素參考檔案：
