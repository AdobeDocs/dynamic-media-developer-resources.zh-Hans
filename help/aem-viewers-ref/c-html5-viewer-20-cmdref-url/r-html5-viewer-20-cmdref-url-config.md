---
description: 所有查看器通用的参数。
seo-description: 所有查看器通用的参数。
seo-title: config
solution: Experience Manager
title: 配置
topic: Dynamic Media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---


# config{#config}

所有查看器通用的参数。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>查看器配置的目录/ID。 </p> <p> 指定包含<span class="codeph"> catalog::UserData </span>中查看器配置属性的图像目录条目。 当此命令存在时，查看器将向服务器发送<span class="codeph"> configId </span>的<span class="codeph"> req=userdata </span>命令，并从回复中提取属性。 属性用于初始化查看器。 如果URL字符串指定相同的属性，则它们将覆盖<span class="codeph">目录：:UserData </span>中的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以在`catalog::UserData`中指定的所有查看器命令，其本身应为`asset`、`serverUrl`、`contentUrl`、`searchServerUrl`和`config`。

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无。

## 示例1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

名为2020的图像目录包含条目`preset-oct`。 此目录条目的`catalog::UserData`字段包含以下数据：

```
style=customStyle.css
```

使用以下命令加载查看器：

```
config=2020/preset-oct
```

这等效于在URL中明确指定的以下命令：

```
style=customStyle.css
```

## 示例2 {#section-577fce5ddbee43fc96d88b2055df47aa}

名为2019的图像目录包含条目`spin-oct`。 此目录条目的`catalog::UserData`字段包含以下数据：

```
zoomStep=3 
maxZoom=200
```

使用以下命令加载查看器：

```
config=2019/spin-oct
```

这等效于在URL中明确指定的以下命令：

```
zoomStep=3&maxZoom=200
```

## 示例3 {#section-2b3a42c3926e4eb19fa14434def9195f}

名为`Shoppable_Banner`的查看器预设包含以下数据：

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

使用以下命令加载查看器：

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

这等效于在URL中明确指定的以下命令：

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 示例5 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

名为`Shoppable_Video_Dark`的查看器预设包含以下数据：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

使用以下命令加载查看器：

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

这等效于在URL中明确指定的以下命令：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 示例4 {#section-19b988551d1d492a9079948e0b04b38f}

名为`Carousel_Dotted_light`的查看器预设包含以下数据：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

使用以下命令加载查看器：

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

这等效于在URL中明确指定的以下命令：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

