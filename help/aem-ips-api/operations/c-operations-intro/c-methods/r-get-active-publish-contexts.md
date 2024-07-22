---
description: Hämtar en lista över aktiva publiceringskontexter för det angivna företaget. En publiceringskontext betraktas som aktiv om minst en aktiv server har definierats för kontexten.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# getActivePublishContext{#getactivepublishcontext}

Hämtar en lista över aktiva publiceringskontexter för det angivna företaget. En publiceringskontext betraktas som aktiv om minst en aktiv server har definierats för kontexten.

Syntax

## Auktoriserade användartyper {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-a4be4024e55c472fa6728faec9c5e048}

**Indata (getActivePublishContexterParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Referensen till företaget som frågar efter aktiva publiceringskontexter |

**Utdata (getActivePublishContextReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| contextArray | `types:StringArray` | Ja | Arrayen med aktiva publiceringskontexter, som kan innehålla noll eller flera värden från Publish Context. |
