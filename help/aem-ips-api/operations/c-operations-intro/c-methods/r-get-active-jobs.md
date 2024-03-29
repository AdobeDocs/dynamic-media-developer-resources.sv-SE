---
description: Hämtar alla aktiva jobb.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# getActiveJobs{#getactivejobs}

Hämtar alla aktiva jobb.

Syntax

## Auktoriserade användartyper {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Indata (getActiveJobsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Nej | Handtaget till företaget. |
| jobHandle | `xsd:string` | Nej | Handtaget till jobbet. |
| originalName | `xsd:string` | Nej | Ursprungligt jobbnamn. |

**Utdata (getActiveJobsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| jobArray | `xsd:string` | Ja | Matris med aktiva jobb. |

## Exempel {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Detta kodexempel returnerar alla aktiva jobb för ett företag som kör i IPS. I det här fallet är svaret ovanligt eftersom IPS-schemaläggningskoordinatorn är inaktiverad och inga aktiva jobb körs. Under normala förhållanden returnerar svaret ett antal aktiva jobb.

**Begäran**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Svar**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
