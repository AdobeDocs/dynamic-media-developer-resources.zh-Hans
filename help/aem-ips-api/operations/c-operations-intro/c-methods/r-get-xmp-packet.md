---
description: 检索指定资源的XMP元数据包。
solution: Experience Manager
title: getXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76e595bd-e598-40e8-aba3-b270fcf4d800
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 20%

---

# getXMPPacket{#getxmppacket}

检索指定资源的XMP元数据包。

语法

## 授权用户类型 {#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-b4075df0e4414b00b961d978d5471db9}

**输入(getXMPPacketParam**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要返回的数据包的公司句柄（例如，`c|656`）。 |
| assetHandle | `xsd:string` | 是 | 应为其检索XMP数据包的资源。 |

**输出(getXMPPacketReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 压缩包 | `xsd:Base 64 binary` | 是 | [!DNL zlib-compressed] XMP数据包。 |

## 示例 {#section-d681af49122e4ca9bcd04110a2e98e6f}

**请求**

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**响应**

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```
