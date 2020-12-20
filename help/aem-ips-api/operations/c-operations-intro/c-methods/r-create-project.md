---
description: Skapar ett nytt projekt.
seo-description: Skapar ett nytt projekt.
seo-title: createProject
solution: Experience Manager
title: createProject
topic: Scene7 Image Production System API
uuid: e011b7ba-6c15-47ef-9ea1-6189c37e7719
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget för det företag som är associerat med det nya projektet. |
| ` *`projectName`*` | `xsd:string` | Ja | Nytt projektnamn. |

**Utdata (createProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | Ja | Referensen till det nya projektet. |

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

