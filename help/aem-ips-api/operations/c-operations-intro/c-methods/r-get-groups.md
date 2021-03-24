---
description: Returnerar företagsgrupper.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# getGroups{#getgroups}

Returnerar företagsgrupper.

Syntax

## Auktoriserade användartyper {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-0e06195f23dd4c69922df210f566dd18}

**Indata (getGroupsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |

**Utdata (getGroupsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Ja | Matris med grupper. |

## Exempel {#section-ed0708f611574354bf0c6ea83912b531}

Den här koden returnerar en array som innehåller alla grupper som tillhör ett visst företag och specifik information om varje grupp.

**Begäran**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```

