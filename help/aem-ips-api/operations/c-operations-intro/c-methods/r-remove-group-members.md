---
description: Tar bort företagsanvändare från en viss grupp.
seo-description: Tar bort företagsanvändare från en viss grupp.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembers{#removegroupmembers}

Tar bort företagsanvändare från en viss grupp.

**Skillnader mellan kommandot Ta bort**

* `removeGroupMembers`: Tar bort flera användare från en grupp.
* `removeGroupMembership`: Tar bort en enskild användare från en array med grupper.

## Auktoriserade användartyper {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-b5596614a3be4ce5962455884e4636af}

**Indata (removeGroupMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget med de användare som du vill arbeta med. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppreferens. |
| ` *`userHandleArray`*` | `types:HandleArray` | Ja | En array med handtag för användare vars gruppmedlemskap du vill ta bort. |

**Utdata (removeGroupMembersParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-9eedac852cea46ec80de6a6928bf97ac}

Detta kodexempel tar bort en användare från det angivna företaget. Ta bort flera användare från en grupp med användarhandtagsarrayen.

**Begäran**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Svar**

Ingen.
