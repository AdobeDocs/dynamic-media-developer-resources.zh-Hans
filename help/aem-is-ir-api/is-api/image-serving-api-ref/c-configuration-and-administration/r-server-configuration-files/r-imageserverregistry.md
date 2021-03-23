---
description: 包含图像服务器配置设置。
seo-description: 包含图像服务器配置设置。
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

包含图像服务器配置设置。

修改此XML文件时，必须注意保持有效的XML语法，否则图像服务器可能无法开始。

要使更改生效，请在编辑此文件后重新启动图像服务器。 只有下面列出的元素值才支持修改。 仅在得到Dynamic Media技术支持的建议时编辑此文件的任何其他内容。

>[!NOTE]
>
>请勿更改`<imageserverregistry>`的结构，包括元素的顺序。 编辑此文件时请务必小心，否则图像服务器可能无法开始。

以下说明了可以更改的元素。 存在其他不能更改的元素。 以下元素的顺序不反映文件中元素必须出现的顺序。

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## 说明 {#section-7217f011f69f41e7af4f3983d7776d6f}

可能存在多个`<RootPath>`元素（每个源数据文件文件夹对应一个元素）。 图像服务器按指定的顺序搜索根路径以查找特定源文件。
