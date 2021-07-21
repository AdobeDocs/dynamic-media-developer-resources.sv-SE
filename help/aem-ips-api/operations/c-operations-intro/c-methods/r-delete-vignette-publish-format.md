---
description: Tar bort ett publiceringsformat för vinjettering.
solution: Experience Manager
title: deleteVinjettPublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# deleteVinjettPublishFormat{#deletevignettepublishformat}

Tar bort ett publiceringsformat för vinjettering.

## Auktoriserade användartyper {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-789625ba29df4b5f880914d4c64f77ce}

**Indata (deleteVinjettPublishFormatParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag som vinjetteringen tillhör. |
| `*`vinjetteringFormatHandtag`*` | `xsd:string` | Ja | Referensen till vinjetteringens publiceringsformat som ska tas bort. |

**Utdata (deleteVinjettPublishFormatParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Det här kodexemplet tar bort ett format för vinjettering som anges i dess handtag.

**Begäran**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Svar**

Ingen.
