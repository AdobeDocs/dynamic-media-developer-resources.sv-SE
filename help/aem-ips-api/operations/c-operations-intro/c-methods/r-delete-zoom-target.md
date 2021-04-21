---
description: Tar bort ett zoommål.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# deleteZoomTarget{#deletezoomtarget}

Tar bort ett zoommål.

## Auktoriserade användartyper {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-225330a45e7a408f8375e084677d9cb1}

**Indata (deleteZoomTargetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag som zoommålet tillhör. |
| `*`zoomTargetHandle`*` | `xsd:string` | Ja | Handtaget till zoommålet som ska tas bort. |

**Utdata (deleteZoomTargetParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-a35857a5ca884357a879f7ba6cf985fe}

Det här kodexemplet tar bort ett zoommål från ett företag.

**Begäran**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Svar**

Ingen.
