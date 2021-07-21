---
description: Anger en användares medlemskap i ett eller flera företag.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
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
