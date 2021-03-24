---
description: Tar bort ett publiceringsformat för vinjettering.
solution: Experience Manager
title: deleteVinjettPublishFormat
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
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
