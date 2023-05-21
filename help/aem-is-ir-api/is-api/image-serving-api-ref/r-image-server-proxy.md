---
description: 影像伺服器Proxy可用來調整日文電話的影像大小。
solution: Experience Manager
title: 影像伺服器Proxy
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# 影像伺服器Proxy{#image-server-proxy}

影像伺服器Proxy可用來調整日文電話的影像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS Proxy的URL格式與一般IS要求非常類似。 任何傳遞至Proxy的IS修飾元都會傳遞至影像伺服器。 您可以在IS修飾元的 [HTTP通訊協定參考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxy專用修飾元清單 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定裝置可用寬度的百分比，以做為影像寬度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 海百分比= &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定裝置可用高度的百分比，以做為影像高度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定裝置的記憶體限制內嵌媒體屬性中，回應大小限製為的百分比。 這僅適用於jpg回應。 影像品質會降低，直到回應大小在指定的百分比內為止。 </p></td> 
 </tr> 
</table>

## 內嵌影像記憶體限制 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果裝置具有可內嵌在網頁上的影像大小限制，只要回應格式為jpg，影像大小就會限製為該大小。 如果裝置沒有任何限制，Proxy會將回應限製為500MB。

## 後端處理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Proxy每天會下載、驗證和載入Device Atlas資料檔案一次。 驗證會為不同裝置提取不同屬性，並在接受新資料之前與預期值比較。
