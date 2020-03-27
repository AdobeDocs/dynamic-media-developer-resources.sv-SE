---
description: Startar om ett pausat jobb.
seo-description: Startar om ett pausat jobb.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Scene7 Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# resumeJob{#resumejob}

Startar om ett pausat jobb.

Syntax

## Auktoriserade användartyper {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Indata (resumeJobParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget med det jobb som du vill starta om. |
| ` *`jobHandle`*` | `xsd:string` | Ja | Referensen till det pausade jobbet. |

**Utdata (resumeJobReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-d0524e031f1f43d89430eade19526162}

Detta kodexempel startar om ett pausat jobb.

**Begäran**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Svar**

Ingen.
