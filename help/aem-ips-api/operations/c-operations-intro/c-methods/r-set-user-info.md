---
description: Anger användarattribut (till exempel namn, e-postadress, roll o.s.v.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# setUserInfo{#setuserinfo}

Anger användarattribut (till exempel namn, e-postadress, roll o.s.v.)

Syntax

## Auktoriserade användartyper {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-71b457921fe74acb862a1e112e550211}

**Indata (setUserInfoParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| userHandle | `xsd:string` | Nej | Användarhandtag. |
| firstName | `xsd:string` | Ja | Förnamn. |
| lastName | `xsd:string` | Ja | Efternamn. |
| e-post | `xsd:string` | Ja | E-post från användare. |
| defaultRole | `xsd:string` | Ja | Anger rollen för en användare i varje företag de tillhör. Observera dock att `IpsAdmin` roll åsidosätter andra inställningar per företag. |
| passwordExpires | `xsd:dateTime` | Nej | Ange förfallodatum för lösenord. |
| isValid | `xsd:boolean` | Ja | Avgör om användaren är en giltig IPS-användare. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | En array med företagshandtag. |

**Utdata (setUserInfoReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-272c103076fb4de0a53729e2f6bfb895}

**Begäran**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Svar**

Ingen.
