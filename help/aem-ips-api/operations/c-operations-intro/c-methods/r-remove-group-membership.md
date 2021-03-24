---
description: Tar bort användare från en array med grupper.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# removeGroupMembership{#removegroupmembership}

Tar bort användare från en array med grupper.

**Skillnader mellan kommandot Ta bort**

* `removeGroupMembers`: Tar bort flera användare från en grupp.
* `removeGroupMembership`: Tar bort en enskild användare från en array med grupper.

## Auktoriserade användartyper {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Indata (removeGroupMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nej | Referensen till det företag vars gruppmedlemskap du vill ta bort. |
| `*`groupHandleArray`*` | `types:HandleArray` | Ja | Arrayen med referenser till grupper från vilka du vill ta bort företaget. |

**Utdata (removeGroupMembershipReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-f8d4181170a243efb9faf5824ae96197}

Detta kodexempel tar bort en användare från en grupp.

**Begäran**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Svar**

Ingen.
