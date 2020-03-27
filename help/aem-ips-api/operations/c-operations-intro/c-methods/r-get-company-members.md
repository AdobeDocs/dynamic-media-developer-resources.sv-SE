---
description: Returnerar användarna för ett företag som anges av en företagsreferens.
seo-description: Returnerar användarna för ett företag som anges av en företagsreferens.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Scene7 Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyMembers{#getcompanymembers}

Returnerar användarna för ett företag som anges av en företagsreferens.

Syntax

## Auktoriserade användartyper {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-5602e4d6f2214e398e6a804e61f1a088}

**Indata (getCompanyMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars medlemmar du vill få. |
| ` *`includeInvalid`*` | `xsd:boolean` | Ja | Inkludera ogiltiga företag. |

**Utdata (getCompanyMembersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`memberArray`*` | `types:CompanyMemberArray` | Ja | En matris med användarmedlemskap. |

## Exempel {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Detta kodexempel returnerar alla medlemmar i ett företag i en användararray. Svaret har trunkerats av kortfattade skäl.

**Begäran**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Svar**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

