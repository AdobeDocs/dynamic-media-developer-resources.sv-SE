---
description: Stoppar ett pågående jobb.
seo-description: Stoppar ett pågående jobb.
seo-title: stopJob
solution: Experience Manager
title: stopJob
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# stopJob{#stopjob}

Stoppar ett pågående jobb.

Syntax

## Auktoriserade användartyper {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-2b64f074e37c4c38849994f3bc65342a}

**Indata (stopJobParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`jobHandle`*` | `xsd:string` | Ja | Hantera jobbet som du vill stoppa. |

**Utdata (stopJobReturn0**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Begäran**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Svar**

Ingen.
