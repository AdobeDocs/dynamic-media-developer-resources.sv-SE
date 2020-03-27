---
description: Hämtar en lista över aktiva publiceringskontexter för det angivna företaget. En publiceringskontext betraktas som aktiv om minst en aktiv server har definierats för kontexten.
seo-description: Hämtar en lista över aktiva publiceringskontexter för det angivna företaget. En publiceringskontext betraktas som aktiv om minst en aktiv server har definierats för kontexten.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActivePublishContext{#getactivepublishcontext}

Hämtar en lista över aktiva publiceringskontexter för det angivna företaget. En publiceringskontext betraktas som aktiv om minst en aktiv server har definierats för kontexten.

Syntax

## Auktoriserade användartyper {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-a4be4024e55c472fa6728faec9c5e048}

**Indata (getActivePublishContextParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som frågar efter aktiva publiceringskontexter |

**Utdata (getActivePublishContextReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Ja | Arrayen med aktiva publiceringskontexter, som kan innehålla noll eller flera värden från Publish Context. |

