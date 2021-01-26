---
description: getVinjettPublishFormats
solution: Experience Manager
title: getVinjettPublishFormats
topic: Dynamic Media Image Production System API
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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

**Indata (getVinjettPublishFormatsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |

**Utdata (getVinjettPublishFormatsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | Ja | Array med publiceringsformat för vinjettering. |

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

