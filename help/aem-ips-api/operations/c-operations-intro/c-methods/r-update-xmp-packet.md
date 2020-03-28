---
description: 设置或更新资产的XMP元数据包。
seo-description: 设置或更新资产的XMP元数据包。
seo-title: updateXMPPacket
solution: Experience Manager
title: updateXMPPacket
topic: Scene7 Image Production System API
uuid: 97a40261-8f85-4e8c-8aa5-ed4fec297f33
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateXMPPacket{#updatexmppacket}

设置或更新资产的XMP元数据包。

语法

## 授权用户类型 {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalcontribUser`

## 参数 {#section-7a89621d441840faba639746b410a489}

**输入(updateXMPPacketParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| ` *`compressedPacket`*` | `xsd:Base 64 binary` | 是 | [!DNL zlib-compressed] 要设置或更新的XMP包。 |

**输出(updateXMPPacketReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`成功`*` | `xsd:boolean` | 是 | 返回 `true` 包是否已更新。 |

## 示例 {#section-38b556b94e5044bf97a954519ff6c212}

**请求**

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**响应**

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```

