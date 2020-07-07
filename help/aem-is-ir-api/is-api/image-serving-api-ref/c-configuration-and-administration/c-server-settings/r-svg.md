---
description: 仅当需要SVG渲染时，才需要考虑本节中的设置。
seo-description: 仅当需要SVG渲染时，才需要考虑本节中的设置。
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# SVG{#svg}

仅当需要SVG渲染时，才需要考虑本节中的设置。

## SV::SvgHeapSize - SVG堆大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG渲染器的Java堆大小。 默认为“200m”(200 MB)。

## PS::svgProvider.rootPaths - SVG数据根文件夹 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源数据文件的位置。 可以是一个或多个相对的绝对文件路径或路径， *[!DNL install_folder]*&#x200B;以分号分隔。 通常设置为与相同的值 `IS::RootPath`。

## PS::svgProvider.SVGileSizeLimit —— 最大SVG文件大小 {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源文件大小（以千字节为单位）。 当尝试渲染大于此限制的SVG文件时，服务器返回错误。 默认值为1024千字节。

## IS::SvgMAxRenderRgnPixels - SVG输出图像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

限制SVGRender可生成的图像的大小。 大于0的整数值（以百万像素为单位）。 如果渲染操作超过大小限制，则返回错误。 默认值为 4。

## PS::svgProvider.port —— 平台服务器监听端口 {#section-f7e42a96c2dd4523b46f0557c239e659}

用于SvgRender的端口，用于从平台服务器获取要嵌入到SVG渲染中的图像。

重要信息要使SVGRender组件正常工作，必须将此配置选项设置为与相同的值 `TC::PsPort`。

## PS::svgProvider.fontRoot - SVG字体文件文件夹 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender将在何处找到渲染SVG文本所需的字体文件； 通常是中指定的路径之一 `IS::RootPaths`。 默认值为[!DNL *[!DNL install_folder]*/图像]。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG通信端口 {#section-608687123aa644b7b58fe42385d71b79}

配置图像服务器和SVGRender组件通信的端口。

>[!NOTE]
>
>要使SVGRender组件正常工作，必须为和指定相同的端 `SVG::SVGRender.port` 口号 `IS::SVGTcpPort`。

