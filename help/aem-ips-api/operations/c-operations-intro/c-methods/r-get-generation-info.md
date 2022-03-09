---
description: Returnerar två olika typer av information baserat på de parametrar som skickats. OriginatorHandle returnerar information om resurser som genererats från den angivna resursen. generateHandle returnerar information om steg som används för att generera den angivna resursen eller filen.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# getGenerationInfo{#getgenerationinfo}

Returnerar två olika typer av information baserat på de parametrar som skickats. OriginatorHandle returnerar information om resurser som genererats från den angivna resursen. generateHandle returnerar information om steg som används för att generera den angivna resursen eller filen.

Syntax

## Auktoriserade användartyper {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-b7fa94c82147455888e8469fa5f6922b}

**Indata (getGenerationInfoParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| Kodfras | `xsd:string` | Ja | Handtaget till företaget. |
| Kodfras | `xsd:string` | Nej | Motorn som användes i generationen. Se Teckensnittsformat. |
| Kodfras | `xsd:string` | Nej | Referensen för resursen som ska frågas efter genererade resurser. |
| Kodfras | `xsd:string` | Nej | Handtaget för resursen som ska efterfrågas efter resurser och motorer som används vid genereringen. |
| Kodfras | `xsd:StringArray` | Nej | Egenskaper som ingår i åtgärden. |
| Kodfras | `xsd:StringArray` | Nej | Egenskaper som är exkluderade från åtgärden. |

**Utdata (getGenerationInfoReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | Ja | Array med genereringsinformation. |

## Exempel {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Det här kodexemplet returnerar information om resurser som genererats från en viss resurs. Den hämtar inte information om steg som används för att generera den angivna resursen. Svaret kortas av för att vara kortfattat.

**Begäran**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Svar**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
