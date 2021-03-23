---
description: Anger en användares medlemskap i ett eller flera företag.
seo-description: Anger en användares medlemskap i ett eller flera företag.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# setCompanyMembership{#setcompanymembership}

Anger en användares medlemskap i ett eller flera företag.

Syntax

## Auktoriserade användartyper {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-3930dc6a016140178631083563598104}

**Indata (setCompanyMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | Nej | Användarhandtag. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Array med företag. |

**Utdata (setCompanyMembershipParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-862c0cc32ce0407ab248028e690a8386}

Det här kodexemplet lägger till en användare i ett företag. Ange vid behov flera företag i företagsmatrisen.

**Begäran**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Svar**

Ingen.
