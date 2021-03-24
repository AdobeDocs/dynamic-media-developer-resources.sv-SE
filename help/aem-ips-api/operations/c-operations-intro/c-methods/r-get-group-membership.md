---
description: Returnerar medlemmarna i en grupp.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# getGroupMembership{#getgroupmembership}

Returnerar medlemmarna i en grupp.

Syntax

## Auktoriserade användartyper {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-2e92f850254e46e48403acaa215341a5}

**Indata (getGroupMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nej | Referensen till användaren. |
| `*`companyHandle`*` | `xsd:string` | Nej | Handtaget till företaget. |

**Utdata (getGroupMembershipReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Matris med grupper. |

## Exempel {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Detta kodexempel returnerar alla medlemmar i en grupp. Eftersom hanterarna för företag och användare är valfria kan åtgärden returnera alla medlemmar i alla grupper.

**Begäran**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Svar**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

