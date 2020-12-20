---
description: Lägger till en användare i ett eller flera företag.
seo-description: Lägger till en användare i ett eller flera företag.
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# addCompanyMembership{#addcompanymembership}

Lägger till en användare i ett eller flera företag.

Syntax

## Auktoriserade användartyper {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Indata (addCompanyMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nej | Referensen till den användare vars medlemskap du vill lägga till. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | En array med företag som du lägger till användaren i. |

**Utdata (addCompanyMembershipReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-5469f88bac7047cca131faa6b021e437}

I det här exemplet används ` *`companyHandleArray`*` för att lägga till en användare i ett enskilt företag.

**Begäran**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Svar**

Ingen.
