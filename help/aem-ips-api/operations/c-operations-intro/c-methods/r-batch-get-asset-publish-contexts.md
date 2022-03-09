---
description: Returnerar publiceringskontexterna för resurser som har markerats för publicering.
solution: Experience Manager
title: batchGetAssetPublishConTexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
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
| companyHandle | `xsd:string` | Ja | Handla till företaget. |
| assetHandleArray | ` `typer:HandleArray&quot; | Ja | En lista med resurser som du vill fråga efter aktiva (markerade för publicering) kontexter. |

**Utdata (batchGetAssetPublishContextReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| assetPublishContextArray | `types:assetPublishContextsArray` | Ja | En array med publiceringskontexter där varje resurs markeras för publicering. |

## Exempel {#section-457f6809ccfa425b9a0976313d613f4e}

**Begäran**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Svar**

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
