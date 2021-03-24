---
description: Byter namn på ett projekt.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# renameProject{#renameproject}

Byter namn på ett projekt.

Syntax

## Auktoriserade användartyper {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-43ccd77648784be4a259a723c3e1db40}

**Indata (renameProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Ja | Hantera företaget med det projekt som du vill byta namn på. |
| `*`projectHandle`*` | `xsd:string` | Ja | Hantera projektet. |
| `*`projectName`*` | `xsd:string` | Ja | Nytt projektnamn. |

**Utdata (renameProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Ja | Referensen för det omdöpta projektet. |

## Exempel {#section-a0a06d9244774795b695a10b92b2a5e7}

Detta kodexempel byter namn på ett projekt och returnerar projektreferensen.

**Begäran**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Svar**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

