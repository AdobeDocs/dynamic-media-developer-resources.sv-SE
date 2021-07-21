---
description: Returnerar användarna för ett företag som anges av en företagsreferens.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars medlemmar du vill få. |
| `*`includeInvalid`*` | `xsd:boolean` | Ja | Inkludera ogiltiga företag. |

**Utdata (getCompanyMembersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | Ja | En matris med användarmedlemskap. |

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
