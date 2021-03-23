---
description: Pausar ett aktivt jobb.
seo-description: Pausar ett aktivt jobb.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# pauseJob{#pausejob}

Pausar ett aktivt jobb.

Syntax

## Auktoriserade användartyper {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Indata (pauseJobParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| `*`jobHandle`*` | `xsd:string` | Ja | Hantera jobbet som du vill pausa. |

**Utdata (PauseJobReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-ee4914f9496f4bd88556728a48fb22c1}

Detta kodexempel pausar ett aktivt jobb.

**Begäran**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Svar**

Ingen.
