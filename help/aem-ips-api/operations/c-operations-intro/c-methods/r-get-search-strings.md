---
description: Hämtar söksträngar, nyckelord och annan information om en resurs. Svaret innehåller ytterligare information om resursen.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# getSearchStrings{#getsearchstrings}

Hämtar söksträngar, nyckelord och annan information om en resurs. Svaret innehåller ytterligare information om resursen.

Syntax

## Auktoriserade användartyper {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-c1efda4bb15349a68b276bafee8c18fd}

**Indata (getSearchStringsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handla till företaget. |
| assetHandle | `xsd:string` | Ja | Hantera tillgången. |

**Utdata (getSearchStringsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | Ja | En array med resurssökningssträngar. |

## Exempel {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Detta kodexempel returnerar resursspecifika söksträngar. Svaret returnerar en tom array.

**Begäran**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Svar**

Ingen.
