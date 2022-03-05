---
description: Ställer in kommandona för Image Serving eller Image Rendering för den angivna resursen. Dessa kommandon ändrar representationen av resursen utan att förstöra den.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# setUrlModifier{#seturlmodifier}

Ställer in kommandona för Image Serving eller Image Rendering för den angivna resursen. Dessa kommandon ändrar representationen av resursen utan att förstöra den.

För bildvisning finns kommandona i `urlModifier` -parametern publiceras i fältet Modifierarkatalog och tillämpas före eventuella kommandon som anges på begärans URL. Kommandon i `urlPostApplyModifier` publiceras på `PostModifier` katalogfält och åsidosätt kommandon på begärande URL eller i `urlModifier`. För bildåtergivning finns kommandona i `urlModifier` och `urlPostApplyModifier` är sammanfogade och publicerade i fältet Modifierarkatalog.

## Auktoriserade användartyper {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Indata (setUrlModifierParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resurshandtag. |
| `*`urlModifier`*` | `xsd:string` | Nej | Protokollkommandon för bildserver eller bildåtergivning som ska användas före begäran eller `urlPostApplyModifier` kommandon. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nej | Protokollkommandon för bildserver eller bildåtergivning som ska användas efter `urlModifier` och begär kommandon. |

**Utdata (setUrlModifierReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Begäran**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Svar**

Ingen.
