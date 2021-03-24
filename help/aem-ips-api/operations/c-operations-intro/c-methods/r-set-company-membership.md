---
description: Anger en användares medlemskap i ett eller flera företag.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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
