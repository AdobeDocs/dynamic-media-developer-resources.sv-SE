---
description: Lägger till användare från ett visst företag i en viss grupp.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# addGroupMembers{#addgroupmembers}

Lägger till användare från ett visst företag i en viss grupp.

Syntax

## Auktoriserade användartyper {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-b28434dcf2ca4b4ea431136aac33913e}

**Indata (addGroupMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget. |
| groupHandle | `xsd:string` | Ja | Grupphandtaget. |
| userHandleArray | `types:HandleArray` | Ja | En array med referenser till användare som du vill lägga till i en grupp. |

**Utdata (addGroupMembersParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-8f168b528aef4c4fa8c3d41f7686842f}

I det här exemplet används addGroupMembersParam för att lägga till en användare i ett enskilt företag. IPS API returnerar inget svar för den här åtgärden.

**Begäran**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Svar**

Ingen.
