---
description: Pausar ett aktivt jobb.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
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
| companyHandle | `xsd:string` | Ja | Handla till företaget. |
| jobHandle | `xsd:string` | Ja | Hantera jobbet som du vill pausa. |

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
