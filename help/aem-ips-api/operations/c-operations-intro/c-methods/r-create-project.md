---
description: Skapar ett nytt projekt.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# createProject{#createproject}

Skapar ett nytt projekt.

Syntax

## Auktoriserade användartyper {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-8c741884eb54489bbaad0c444fee80b6}

**Indata (createProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget för det företag som är associerat med det nya projektet. |
| `*`projectName`*` | `xsd:string` | Ja | Nytt projektnamn. |

**Utdata (createProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Ja | Referensen till det nya projektet. |

## Exempel {#section-a0cd532b67e346d088fbec141231a0e5}

Det här kodexemplet skapar ett projekt med namnet `ApiTestProject` i ett företag som anges av dess referens. Svaret returnerar referensen till projektet.

**Begäran**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```
