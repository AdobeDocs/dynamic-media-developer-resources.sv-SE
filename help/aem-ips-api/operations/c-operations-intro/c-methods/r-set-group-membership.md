---
description: Anger gruppmedlemskap för en användare.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setGroupMembership{#setgroupmembership}

Anger gruppmedlemskap för en användare.

Syntax

## Auktoriserade användartyper {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Indata (setGroupMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| userHandle | `xsd:string` | Nej | Referensen till användaren vars gruppmedlemskap du vill ange. |
| companyHandle | `xsd:string` | Nej | Företagshandtag. |
| groupHandleArray | `types:HandleArray` | Ja | Arrayen med referenser till grupper som användaren tillhör. |

**Utdata (setGroupMembershipReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-67b86d259df24938896fe19061845811}

Detta kodexempel gör användaren till medlem i en grupp. Lägg till en användare i flera grupper med grupphandtagsarrayen.

**Begäran**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Svar**

Ingen.
