---
description: getPublishContexts
solution: Experience Manager
title: getPublishContexts
topic: Dynamic Media Image Production System API
uuid: 7eb90f2c-2bfc-4d61-8a24-831964ed9182
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 24%

---


# getPublishContexts{#getpublishcontexts}

语法

## 授权用户类型{#section-1a3a50349b5640dd8e498ff9e9c37340}

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
>* 用户必须具有读取权限才能返回资产。
>* 所有用户都有权访问共享公司。

>



## 参数 {#section-d08e2175d3f84774b55b91bc590b8b3f}

**输入(getPublishContextsParam)**

<table id="table_4A505A067586464B99F8F68E3B1BE75E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 处理公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">要返回的发布上下文的类型。 包括： 
    <ul id="ul_21EDF8F0026E402EAE8226A0CADEE652">
     <li id="li_06DB502952D943198F16C06C59816268"><span class="codeph"> 图像服务</span></li>
     <li id="li_E67A42934E8F4689A148CE125F7372AE"><span class="codeph"> 图像渲染</span></li>
     <li id="li_3CB3A9C4E7AB4A71819567A9566E396C"><span class="codeph"> 视频</span></li>
     <li id="li_27E3DB89B53B4B50B2231622A157A228"><span class="codeph"> ServerDirectory</span></li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

**输出(getPublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`publishContextArray`*` | types:PublishContextArray | 是 | 公司的发布上下文数组，根据上下文类型进行筛选（如果需要）。 |

## 示例 {#section-23fb7d6a15004b7eb4c3d3bcb37ceb04}

**请求**

```java
<getPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
</getPublishContextsParam>
```

**响应**

```java
<getPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
  <publishContextArray>
    <items>
      <contextHandle>pc|3001</contextHandle>
      <contextName>ImageRendering</contextName>
      <contextType>ImageRendering</contextType>
    </items>
    <items>
      <contextHandle>pc|3002</contextHandle>
      <contextName>ImageServing</contextName>
      <contextType>ImageServing</contextType>
    </items>
    <items>
      <contextHandle>pc|3003</contextHandle>
      <contextName>ServerDirectory</contextName>
      <contextType>ServerDirectory</contextType>
    </items>
    <items>
      <contextHandle>pc|3004</contextHandle>
      <contextName>Video</contextName>
      <contextType>Video</contextType>
    </items>
  </publishContextArray>
</getPublishContextsReturn>
```

