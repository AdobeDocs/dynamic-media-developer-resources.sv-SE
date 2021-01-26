---
description: Hämtar en lista med tecken som används i ett visst fält.
seo-description: Hämtar en lista med tecken som används i ett visst fält.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Dynamic Media Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# getUserChars{#getuserchars}

Hämtar en lista med tecken som används i ett visst fält.

Syntax

## Auktoriserade användartyper {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Indata (getUserCharsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | Ja | Anger vilket papperskorgsläge som ska sökas efter. |
| `*`includeInactive`*` | `xsd:boolean` | Ja | Inkludera eller exkludera inaktiva användare. Användare av icke-IPS-administratörer måste vara en aktiv medlem i minst ett företag för att kunna auktoriseras att göra API-anrop. Ett auktoriseringsfel returneras om användaren inte har några aktiva företagsmedlemskap. |
| `*`includeInvalid`*` | `xsd:boolean` | Nej | Inkludera eller exkludera ogiltiga användare. |
| `*`companyHandleArray`*` | `types:HandleArray` | Nej | Filtrera resultat baserat på företag. |
| `*`groupHandleArray`*` | `types:HandleArray` | Nej | Filtrerar resultat baserat på grupper. |
| `*`userRoleArray`*` | `types:StringArray` | Nej | Filtrerar resultat baserat på användarroll. |
| `*`numChars`*` | `xsd:int` | Nej | Aktivera >1 tecken. |

**Utdata (getUserCharsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Ja | En array med teckenprefix. |

## Exempel {#section-3702f165e8b041139a6144f4a76ca25f}

Detta kodexempel returnerar:

* De första tecknen i efternamnen för användarna i ett visst företag.
* En uppsättning grupper.
* En uppsättning användarroller.

Strängkonstanten User Char Filter Fields bestämmer vilken typ av användartecken som returneras.

**Begäran**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Svar**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

