---
description: Hämtar projekt för en grupp med relaterade resurser.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# getProjects{#getprojects}

Hämtar projekt för en grupp med relaterade resurser.

Syntax

## Auktoriserade användartyper {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-8d549237b8c440b4872a0a086ddc00a1}

**Indata (getProjectsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |

**Utdata (getProjectsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Ja | Arrayen med projekt som är associerade med företaget. |

## Exempel {#section-8b12d0b948f644f68bf9a16060d3849a}

Detta kodexempel returnerar alla projektreferenser i en projektarray.

**Begäran**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Svar**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

