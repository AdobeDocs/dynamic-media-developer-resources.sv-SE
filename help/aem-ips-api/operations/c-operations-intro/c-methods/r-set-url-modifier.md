---
description: Ställer in kommandona för Image Serving eller Image Rendering för den angivna resursen. Dessa kommandon ändrar representationen av resursen utan att förstöra den.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# setUrlModifier{#seturlmodifier}

Ställer in kommandona för Image Serving eller Image Rendering för den angivna resursen. Dessa kommandon ändrar representationen av resursen utan att förstöra den.

För Bildservrar publiceras kommandon i parametern `urlModifier` i katalogfältet Modifierare och används före kommandon som anges på begärande-URL:en. Kommandon i `urlPostApplyModifier` publiceras i katalogfältet `PostModifier` och åsidosätter kommandon i begärande-URL:en eller i `urlModifier`. För bildåtergivning är kommandona i `urlModifier` och `urlPostApplyModifier` sammanfogade och publicerade i fältet Modifierarkatalog.

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
| `*`urlModifier`*` | `xsd:string` | Nej | Image Serving- eller Image Rendering-protokollkommandon som ska användas före begäran eller `urlPostApplyModifier`-kommandon. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nej | Protokollkommandon för bildserver eller bildåtergivning som ska användas efter `urlModifier` och begära kommandon. |

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
