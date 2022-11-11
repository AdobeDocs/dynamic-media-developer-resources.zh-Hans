---
description: 仅当需要渲染SVG时，才需要考虑此部分中的设置。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# SVG{#svg}

仅当需要渲染SVG时，才需要考虑此部分中的设置。

## SV::SvgHeapSize -SVG堆大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG呈现器的Java堆大小。 默认为“200米”(200 MB)。

## PS::svgProvider.rootPaths -SVG数据根文件夹 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源数据文件的位置。 可以是相对于 *[!DNL install_folder]*，以分号分隔。 通常设置为与 `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit — 最大SVG文件大小 {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源文件大小（千字节）。 当尝试渲染大于此限制的SVG文件时，服务器会返回错误。 默认为1024千字节。

## IS::SvgMAxRenderRgnPixels -SVG输出图像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

限制SVGRender可生成的图像的大小。 大于0的整数值（以百万为单位）。 如果渲染操作超出大小限制，则会返回错误。 默认值为 4。

## PS::svgProvider.port - [!DNL Platform Server] 侦听端口 {#section-f7e42a96c2dd4523b46f0557c239e659}

用于SvgRender从 [!DNL Platform Server] 嵌入到SVG渲染中。

重要信息要使SVGRender组件正确运行，必须将此配置选项设置为与 `TC::PsPort`.

## PS::svgProvider.fontRoot -SVG字体文件文件夹 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender将在何处查找渲染SVG文本所需的字体文件；通常是 `IS::RootPaths`. 默认值为[!DNL  *[!DNL install_folder]*/images]。

## SVG::SVGRender.port， IS::SVGTcpPort -SVG通信端口 {#section-608687123aa644b7b58fe42385d71b79}

配置Image Server和SVGRender组件通信的端口。

>[!NOTE]
>
>要使SVGRender组件正确运行，必须为 `SVG::SVGRender.port` 和 `IS::SVGTcpPort`.
