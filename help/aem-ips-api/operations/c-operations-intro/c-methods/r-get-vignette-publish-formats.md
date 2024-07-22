---
description: getVinjettPublishFormats
solution: Experience Manager
title: getVinjettPublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# getVinjettPublishFormats{#getvignettepublishformats}

Syntax

## Auktoriserade användartyper {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Indata (getVignettePublishFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget. |

**Utdata (getVinjettPublishFormatsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | Ja | Array med publiceringsformat för vinjettering. |

## Exempel {#section-2cc32b27cc6243b7b3e273cc05996226}

Detta kodexempel returnerar två vinjetteringsformat som är kopplade till ett visst företag. Informationen returneras i en array, som trunkeras för att vara kortfattad.

**Begäran**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Svar**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
