---
description: Hämtar de användare som tillhör ett visst företag och en viss grupp.
seo-description: Hämtar de användare som tillhör ett visst företag och en viss grupp.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Dynamic Media Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# getGroupMembers{#getgroupmembers}

Hämtar de användare som tillhör ett visst företag och en viss grupp.

Syntax

## Auktoriserade användartyper {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-b798b06354c946abbb90fa72cc9c67fd}

**Indata (getGroupMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| `*`groupHandle`*` | `xsd:string` |  | Referensen till gruppen. |

**Utdata (getGroupMembersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Ja | En array med användarhandtag. |

## Exempel {#section-aaa340dba6b64cce9bcd8303cf999166}

Detta kodexempel returnerar en användarhandtagsarray som innehåller alla användare som tillhör en viss grupp.

**Begäran**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Svar**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

