---
description: 使用這些伺服器設定來設定您的伺服器。
solution: Experience Manager
title: 服务器
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 服务器{#server}

使用這些伺服器設定來設定您的伺服器。

## SV：：ImageServerMode — 影像伺服器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

影像伺服器的32位元和64位元版本均適用於Linux。 若安裝在64位元Linux伺服器上，請指定ImageServer64；若安裝在32位元伺服器上，請指定ImageServer32 （預設）。

>[!NOTE]
>
>64位元版本的Image Server不支援FlashPix來源檔案。

>[!NOTE]
>
>Windows不支援64位元模式。 僅限 `ImageServer32` 可指定。 否則將不會啟動影像伺服。

## SV：：PsHeapSize - [!DNL Platform Server] 棧積大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

的Java棧積大小 [!DNL Platform Server]. 預設為&quot; `512m`「 (512 MB)。

## IS：：TcpPort， PS：：isConnection.port — 影像伺服器接聽連線埠 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用於通訊的通訊埠 [!DNL Platform Server] 和影像伺服器。 請務必指定在主機系統上不會使用的連線埠號碼。

>[!NOTE]
>
>若要讓「影像伺服」正常運作，必須設定相同的值 `IS::TcpPort` 和 `PS::isConnection.port`.

## IS：：PhysicalMemory — 影像伺服器記憶體限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

記憶體內部影像資料的大約限制，以實體記憶體的百分比表示。 有效範圍為10%到90%。 影像伺服器會儘可能將影像記憶體的使用限制在指定的數量。 在繁重處理作業期間，可能會暫時超過限制。

## IS：：WorkerThreads — 影像伺服器工作執行緒數目 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

影像伺服器用於處理影像資料的最大執行緒數量。 預設值為0，可讓影像伺服器自動最佳化執行緒計數。

某些作業系統有執行緒模型，而且內容交換開銷很高。 在這種情況下，選取特定執行緒計數時（例如每個CPU一個執行緒），整體伺服器效能可能會改善。 可能需要一些實驗來尋找最佳設定。 如需詳細資訊，請參閱「影像伺服」發行說明和作業系統檔案。

## IS：：NumberOfTextServers — 文字伺服器執行個體數目 {#section-971e20a90c1a473598fba738ed95671a}

同時作用中的文字轉譯器數目上限。 0 （預設）等於可用CPU核心數的1.5倍。

## IS：：TextServerTcpPortRange — 文字伺服器通訊連線埠 {#section-a13465de88ed4df09931e5ba840c1942}

用於文字伺服器通訊的連線埠。 指定第一個和最後一個連線埠號碼，以&#39;-&#39;分隔。
