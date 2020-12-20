---
description: Hämtar projekt för en grupp med relaterade resurser.
seo-description: Hämtar projekt för en grupp med relaterade resurser.
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Scene7 Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |

**Utdata (getProjectsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`projectArray`*` | `types:ProjectArray` | Ja | Arrayen med projekt som är associerade med företaget. |

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

