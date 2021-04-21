---
description: Tar bort en användare från ett eller flera företag.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# removeCompanyMembership{#removecompanymembership}

Tar bort en användare från ett eller flera företag.

Syntax

## Auktoriserade användartyper {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Indata (removeCompanyMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nej | Referensen till användaren med det medlemskap du vill ta bort. |
| `*`companyHandleArray`*` | `types:HandleArray` | Ja | Referensen till företaget som du tar bort användaren från. |

**Utdata (removeCompanyMembershipReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-6b7903195e8647a1bd0502f87387ca62}

Det här kodexemplet tar bort en användare från ett företag. Utelämna den valfria användarreferensen för att ta bort alla användare från de företag som anges i företagsreferensarrayen.

**Begäran**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Svar**

Ingen.
