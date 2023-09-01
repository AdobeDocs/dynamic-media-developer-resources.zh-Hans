---
title: SVG
description: 仅当需要SVG渲染时，才必须考虑此部分中的设置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# SVG{#svg}

仅当需要SVG渲染时，才必须考虑此部分中的设置。

## SV：：SvgHeapSize -SVG栈大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG渲染器的Java栈大小。 默认为“200m”(200 MB)。

## PS：：svgProvider.rootPaths -SVG数据根文件夹 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源数据文件的位置。 它可以是相对于的一个或多个绝对文件路径或路径 *[!DNL install_folder]*，以分号分隔。 通常设置为与相同的值 `IS::RootPath`.

## PS：：svgProvider.SVGFileSizeLimit — 最大SVG文件大小 {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源文件大小（千字节）。 尝试渲染大于此限制的SVG文件时，服务器返回错误。 默认值为1024 KB。

## IS：：SvgMAxRenderRgnPixels -SVG输出图像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

它限制了SVGRender可以生成的图像的大小。 大于0的整数值（百万像素）。 如果渲染操作超出大小限制，则返回错误。 默认值为 4。

## PS：：svgProvider.port - [!DNL Platform Server] 侦听端口 {#section-f7e42a96c2dd4523b46f0557c239e659}

用于SvgRender从获取图像的端口 [!DNL Platform Server] 嵌入到SVG渲染中。

重要信息：要使SVGRender组件正常工作，必须将此配置选项设置为与相同的值 `TC::PsPort`.

## PS：：svgProvider.fontRoot — 字体文件SVG文件夹 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender在何处查找渲染SVG文本所需的字体文件；通常为中指定的路径之一 `IS::RootPaths`. 默认值为[！DNL  *[!DNL install_folder]*/images]。

## SVG：：SVGRender.port， IS：：SVGTcpPort -SVG通信端口 {#section-608687123aa644b7b58fe42385d71b79}

配置图像服务器和SVGRender组件进行通信的端口。

>[!NOTE]
>
>要使SVGRender组件正常工作，必须为指定相同的端口号 `SVG::SVGRender.port` 和 `IS::SVGTcpPort`.
