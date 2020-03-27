---
description: Anger användarattribut (t.ex. namn, e-postadress, roll)
seo-description: Anger användarattribut (t.ex. namn, e-postadress, roll)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUserInfo{#setuserinfo}

Anger användarattribut (t.ex. namn, e-postadress, roll)

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
| ` *`userHandle`*` | `xsd:string` | Nej | Användarhandtag. |
| ` *`firstName`*` | `xsd:string` | Ja | Förnamn. |
| ` *`lastName`*` | `xsd:string` | Ja | Efternamn. |
| ` *`e-post`*` | `xsd:string` | Ja | E-post från användare. |
| ` *`defaultRole`*` | `xsd:string` | Ja | Anger rollen för en användare i varje företag de tillhör. Observera dock att `IpsAdmin` rollen åsidosätter andra inställningar per företag. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Nej | Ange förfallodatum för lösenord. |
| ` *`isValid`*` | `xsd:boolean` | Ja | Avgör om användaren är en giltig IPS-användare. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | En array med företagshandtag. |

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
