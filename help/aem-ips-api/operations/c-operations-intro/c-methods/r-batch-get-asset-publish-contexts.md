---
description: Returnerar publiceringskontexterna för resurser som har markerats för publicering.
seo-description: Returnerar publiceringskontexterna för resurser som har markerats för publicering.
seo-title: batchGetAssetPublishConTexts
solution: Experience Manager
title: batchGetAssetPublishConTexts
topic: Scene7 Image Production System API
uuid: 7f442019-37a9-4473-be92-a952a7a67664
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# batchGetAssetPublishConTexts{#batchgetassetpublishcontexts}

Returnerar publiceringskontexterna för resurser som har markerats för publicering.

Syntax

## Auktoriserade användartyper {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* Användaren måste ha läsåtkomst för att kunna returnera resurserna.
>* Alla användare har åtkomst till det delade företaget.

>



## Parametrar {#section-1742fcb196224545b270eb8241f757a8}

**Indata (batchGetAssetPublishContexterParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| ` *`assetHandleArray`*` | ` `typer:HandleArray&quot; | Ja | En lista med resurser som du vill fråga efter aktiva (markerade för publicering) kontexter. |

**Utdata (batchGetAssetPublishContextReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`assetPublishContextArray`*` | `types:assetPublishContextsArray` | Ja | En array med publiceringskontexter där varje resurs markeras för publicering. |

## Exempel {#section-457f6809ccfa425b9a0976313d613f4e}

**Begäran**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Svar**

```java
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

