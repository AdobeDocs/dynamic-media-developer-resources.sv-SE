---
description: Hämtar schemalagda jobb att köras.
seo-description: Hämtar schemalagda jobb att köras.
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Scene7 Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# getScheduledJobs{#getscheduledjobs}

Hämtar schemalagda jobb att köras.

Syntax

## Auktoriserade användartyper {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-2af604ff8282460990b9237158187f8f}

**Indata (getScheduledJobsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| ` *`jobHandle`*` | `xsd:string` | Nej | Jobbreferens. |
| ` *`originalName`*` | `xsd:string` | Nej | Namnet som anges av `submitJob`. |

**Utdata (getScheduledJobsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`jobArray`*` | `types:ScheduledJobArray` | Ja | Matris med schemalagda jobb. |

## Exempel {#section-e79e7da86ba848fd9996aa36de462e6c}

Detta kodexempel returnerar alla schemalagda jobb i en jobbarray. Arrayen innehåller detaljerad information om jobben.

**Begäran**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Svar**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

