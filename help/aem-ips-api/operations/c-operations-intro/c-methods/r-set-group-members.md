---
description: Anger gruppmedlemskap för användare som tillhör ett visst företag.
seo-description: Anger gruppmedlemskap för användare som tillhör ett visst företag.
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Scene7 Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# setGroupMembers{#setgroupmembers}

Anger gruppmedlemskap för användare som tillhör ett visst företag.

Åtgärden orsakar ett autentiseringsfel om du inte har behörighet att utföra den här åtgärden. Detta gäller även om någon av användarna i användarhandtagsarrayen inte tillhör det företag som anges i företagshandtaget,

## Auktoriserade användartyper {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-6a18562fc8e942af94be10bbb8c51151}

**Indata (setGroupMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppreferens. |
| ` *`userHandleArray`*` | `types:HandleArray` | Ja | Array med referenser för användare vars gruppmedlemskap du vill ange. |

**Utdata (setGroupMembesReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-9c528c3f44a141ce9eaddf634f26c487}

Det här kodexemplet anger gruppmedlemskap för en enskild användare.

**Begäran**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Svar**

Ingen.
