---
description: Tar bort ett projekt från ett företag. Länkarna mellan resurserna och projektet är brutna, men resurserna tas inte bort från IPS.
seo-description: Tar bort ett projekt från ett företag. Länkarna mellan resurserna och projektet är brutna, men resurserna tas inte bort från IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# deleteProject{#deleteproject}

Tar bort ett projekt från ett företag. Länkarna mellan resurserna och projektet är brutna, men resurserna tas inte bort från IPS.

Syntax

## Auktoriserade användartyper {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Indata (deleteProjectParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | Namnet på det företag som är associerat med projektet. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Referensen till det projekt som ska tas bort. |

**Utdata (deleteProjectReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-e38507f1f7ec41b9a625f47390490254}

Det här kodexemplet använder företagshandtaget och projektreferensen som fält i deleteProjectParam som skickas till IPS-webbtjänstservern för att ta bort projektet.

**Begäran**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Svar**

Ingen.
