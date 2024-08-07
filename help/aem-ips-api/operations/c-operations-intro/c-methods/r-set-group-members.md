---
description: Anger gruppmedlemskap för användare som tillhör ett visst företag.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
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
| companyHandle | `xsd:string` | Ja | Företagshandtag. |
| groupHandle | `xsd:string` | Ja | Grupphandtag. |
| userHandleArray | `types:HandleArray` | Ja | Array med referenser för användare vars gruppmedlemskap du vill ange. |

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
