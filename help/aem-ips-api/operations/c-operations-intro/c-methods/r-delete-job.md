---
description: Tar bort ett aktuellt eller schemalagt jobb.
seo-description: Tar bort ett aktuellt eller schemalagt jobb.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Dynamic Media Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# deleteJob{#deletejob}

Tar bort ett aktuellt eller schemalagt jobb.

Syntax

## Auktoriserade användartyper {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Indata (deleteJobParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som jobbet tillhör. |
| `*`jobHandle`*` | `xsd:string` | Ja | Referensen till jobbet som ska tas bort. |

**Utdata**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Detta kodexempel tar bort ett jobb som körs eller är schemalagt att köras i IPS. Den kräver en jobbreferens som du måste hämta från en annan åtgärd.

**Begäran**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Svar**

Ingen.
