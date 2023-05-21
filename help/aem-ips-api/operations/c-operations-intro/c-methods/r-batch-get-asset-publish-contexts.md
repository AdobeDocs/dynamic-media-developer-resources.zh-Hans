---
description: 傳回標籤為發佈的資產的發佈內容。
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

傳回標籤為發佈的資產的發佈內容。

语法

## 授權的使用者型別 {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* 使用者必須擁有讀取存取權才能傳回資產。
>* 所有使用者都可存取共用公司。
>


## 参数 {#section-1742fcb196224545b270eb8241f757a8}

**輸入(batchGetAssetPublishContextsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetHandleArray | ` `型別：HandleArray&quot; | 是 | 您要查詢作用中（標籤為發佈）上下文的資產清單。 |

**輸出(batchGetAssetPublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | 是 | 一個發佈內容陣列，其中每個資產都標示為要發佈。 |

## 示例 {#section-457f6809ccfa425b9a0976313d613f4e}

**请求**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**响应**

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
